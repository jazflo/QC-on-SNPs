# QC-on-SNPs
This tutorial provides general steps to conduct preliminary quality control (**QC**) on SNP datasets in vcf files. The instructions are based on best QC practices reviewed in several sources. Here are some:  
[main source](https://doi.org/10.1002/sim.6605)  
[source](https://currentprotocols.onlinelibrary.wiley.com/doi/10.1002/0471142905.hg0119s68)  
[source](https://pubmed.ncbi.nlm.nih.gov/29484742/)  
[source](https://onlinelibrary.wiley.com/doi/10.1002/gepi.20516)
Note 1. This tutorial requires you to have [vcftools](https://vcftools.github.io/man_latest.html) and [bcftools](https://samtools.github.io/bcftools/) installed beforehand.  
Note 2. Whenever possible, I provide alternative ways of performing the QC steps (i.e. alternative tools or softwares)  
## A useful command before starting QC
It´s a good idea to estimate general stats from your vcf file (hereon referred to as "filename"):
```
bcftools stats -s - filename
```
Note that the second "–" is needed to specify that stats should be estimated for ALL samples in the vcf. Otherwise you can give a list of specific samples. 
## How to perform QC?
Also known as "data pre-processing", best QC practices, require that SNPs go through two stages of filtering in a **specific** order:  
1. Filtering at **SNP** level.
2. Filtering at **sample** level.




