# ShatterSeek 

ShatterSeek is an R package that provides utilities to detect chromothripsis events from 
next-generation sequencing (NGS) data.
It takes as input copy number (CN) and structural variation (SV) calls calculated
with the user preferred method. 
Hence, it is compatible with virtually any CN and SV caller.

The main function of the package, shatterseek,
first uses intrachromosomal SVs to detect clusters of interleaved
rearrangements.
Next, it evaluates a set of statistical criteria in each of these regions.
The output consists of a data frame reporting the value for the statistical criteria used 
and additional information for each chromosome.
ShatterSeek also provides functionalities for the visualization of SV and CN profiles,
thus enabling the visual inspection of the candidate chromothripsis regions detected.
ShatterSeek is fast, with an average running time of ~20s per sample.


Further details about the implementation and  
validation of ShatterSeek
using ~2,600 whole-genome sequencing data sets from The Pan-Cancer Analysis of Whole Genomes (PCAWG) project
can be found in the following publication:

**Comprehensive analysis of chromothripsis in 2,658 human cancers using whole-genome sequencing**

Cortes-Ciriano et al. 2018

All the chromothripsis calls reported in that publication can be visualized at: http://compbio.med.harvard.edu/chromothripsis/

A detailed tutorial illustrating how to use ShatterSeek is provided in ./inst/tutorial/tutorial.pdf

ShatterSeek is free for academic use **only**.

For non-academic use, please email Dr. Tatiana Demidova-Rice at Harvard University Office of Technology Development (tatiana\_demidova-rice@harvard.edu)

# Prerequisites

ShatterSeek is written entirely in R (>= 3.0.1) and depends on the following packages:
methods, BiocGenerics, graph, S4Vectors, GenomicRanges, IRanges, MASS, ggplot2, grid, and gridExtra


# Installation
`$ git clone https://github.com/parklab/ShatterSeek.git`

`$ R CMD INSTALL ShatterSeek-master`

Alternatively you can install ShatterSeek directly from R using devtools:
```R
library(devtools)
install_github("parklab/ShatterSeek")
```

# How to use
Please see the package tutorial (especially section "How to use Shatterkeek")

# Contact
If you have any questions or suggestions please contact us:

Isidro Cortes Ciriano: isidrolauscher at gmail.com or isidro_cortesciriano at hms.harvard.edu

Peter J Park: peter_park at hms.harvard.edu

