# phenoscanner
phenoscanner allows users to query the PhenoScanner database of genotype-phenotype associations from inside R.

## Functions
* phenoscanner - this function allows users to query the PhenoScanner database from inside R 

## Installation
1. install.packages("devtools")
2. library(devtools) 
3. install_github("phenoscanner/phenoscanner")
4. library(phenoscanner)

## Examples 
\# SNP  
res <- phenoscanner(snpquery="rs10840293")  
head(res$results)  
res$snps  

\# Gene  
res <- phenoscanner(genequery="SWAP70")  
head(res$results)  
res$genes  

\# Region  
res <- phenoscanner(regionquery="chr11:9685624-9774538")  
head(res$results)  
res$regions  

\# To query multiple SNPs, genes or regions, please supply a vector of SNPs, genes or regions to snpquery, genequery or regionquery options, respectively. For example, to query multiple SNPs:   
res <- phenoscanner(snpquery=c("rs10840293","rs10"))  
head(res$results)  
res$snps 

## Citations
* Staley JR, et al. PhenoScanner: a database of human genotype-phenotype associations. Bioinformatics 2016;32(20):3207-3209.
* Kamat MA, et al. PhenoScanner V2: an expanded tool for searching human genotype-phenotype associations. Bioinformatics 2019;35(22):4851-4853.

## Terms of use
Please abide by the [terms of use](http://www.phenoscanner.medschl.cam.ac.uk/about/#terms) of PhenoScanner when using this R package.
