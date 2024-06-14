# EGFR-ap
This is Danav' project 

 <p align="center">
<img src="https://github.com/amarinderthind/EGFR-ap/assets/45668229/e93c5f06-8e65-44b5-b000-52297a25effb.png" width=95% height="300">&nbsp; &nbsp; &nbsp; &nbsp;
 
 
</p>
### How to start (Check section, Input file requirements)
Tell me .....more 

##### Steps of the pipeline

Input required is a set of two or more genome sequences in FASTA format. The other input required by the user is “word length (K value)” for which the frequencies of all the words in the sequences are calculated. Users can also specify the Out-group for the construction of the Neighbor-Joining Tree. 

These Sequences are then used to calculate frequencies of words at user-specified word lengths. , each sequence gets its own frequency matrices. There is also an option to visualize the CGR plots. Based on these word frequencies the pair-wise distance (Euclidean-default, or  Square Euclidean, or Manhattan) is calculated between all pairs of sequences in input data. Package integrate other packages where distance matrices can be converted to NJ tree or other and visualized. We provide the option to convert distance matrix into MEGA and phylip distance formats, which is a widely used program for visualization. 

##### Input file requirements

The DNA sequences to be analyzed can be uploaded in the form fasta file. All the sequences must be in FASTA format. Check the example file (Input_recom_SARS_cov2.fasta) for details.  

```
setwd(".")
source('cgat_function.r')
source('distances_n_other.r')
source('cgrplot.r')

file <- "Input_recom_SARS_cov2.fasta"

library("seqinr")
fastafile <- seqinr::read.fasta(file = file, seqtype = "DNA", as.string = TRUE, set.attributes = FALSE)
```

