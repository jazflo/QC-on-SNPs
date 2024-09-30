# QC-on-SNPs
This tutorial provides general steps to conduct preliminary quality control (**QC**) on SNP datasets (vcf files).  
Note 1. This tutorial requires you to have [vcftools](https://vcftools.github.io/man_latest.html) and [bcftools](https://samtools.github.io/bcftools/) installed beforehand.  
Note 2. Whenever possible, I provide alternative ways of performing the steps.
## A few useful commands before starting QC
It´s a good idea to estimate general stats from your vcf file (hereon referred to as "filename"):
```
bcftools stats -s - filename
```
Note that the second "–" is needed to specify that stats should be estimated for ALL samples in the vcf. Otherwise you can give a list of specific samples. 
