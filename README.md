# QC-on-SNPs
This tutorial provides general steps to conduct preliminary quality control (**QC**) on SNP datasets (vcf files).  
Note 1. This tutorial is based on best QC practices reviewed in several sources (in case you want to check them):
[main source](https://doi.org/10.1002/sim.6605)
[source](https://currentprotocols.onlinelibrary.wiley.com/doi/10.1002/0471142905.hg0119s68)
[source](https://pubmed.ncbi.nlm.nih.gov/29484742/)
[source](https://onlinelibrary.wiley.com/doi/10.1002/gepi.20516)

Note 2. This tutorial requires you to have [vcftools](https://vcftools.github.io/man_latest.html) and [bcftools](https://samtools.github.io/bcftools/) installed beforehand.  
Note 3. Whenever possible, I provide alternative ways of performing the steps (ex. alternative tools or softwares)
## A useful command before starting QC
It´s a good idea to estimate general stats from your vcf file (hereon referred to as "filename"):
```
bcftools stats -s - filename
```
Note that the second "–" is needed to specify that stats should be estimated for ALL samples in the vcf. Otherwise you can give a list of specific samples. 
## If you intend to work with Plink software, you can transform a vcf file into plink format like this
```
./plink --vcf vcffile --out vcf_in_plink_format
```
This command executes plink (./plink) takes a vcf file as input (--vcf ) and outputs a file in plink format (--out)

