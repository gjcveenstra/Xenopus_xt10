## Description  
Bioconductor provides genome and gene annotation tools for use in downstream applications. There are three types of bioconductor resources that are necessary for use in combination downstream tools: genome (BSgenome.Xtropicalis.Xenbase.xt10), a transcript database (TxDb.Xtropicalis.Xenbase.xt10), and an organism database(org.Xtropicalis.eg.db). The bioconductor files provided here have been used for analysis of 10x single cell ATAC-seq data with ArchR and the xt10 genome, other packages or applications have not been tested.  

## Description BSgenome
Package: BSgenome.Xtropicalis.Xenbase.xt10  
Title: Xenopus tropicalis genome sequences  
Description: Genome sequences of Xenopus tropicalis (assembly v10.0, Xenbase)  
Version: 0.1  
Author: GJC Veenstra <g.veenstra@science.ru.nl>  
Maintainer: GJC Veenstra <g.veenstra@science.ru.nl>  
Depends: BSgenome (>= 1.56.0)  
Imports: BSgenome  
Suggests:  
License: None  
organism: Xenopus tropicalis  
common_name: tropical clawed frog  
provider: Xenbase  
provider_version: xt10  
release_date: 2020-09-14  
release_name: xt10_0  
source_url: http://www.veenstralab.nl/resources.htm  
biocViews: AnnotationData, Genetics, BSgenome, Xenopus tropicalis  
  
## Install
#Only once, at Linux prompt (specify path to file as necessary):  
R CMD INSTALL "BSgenome.Xtropicalis.Xenbase.xt10_0.1.tar.gz"  
#Only once, in R (specify path to file as necessary)  
install.packages("org.Xtropicalis.eg.db", repos=NULL)  
#it has been installed from the genome directory of xt9_0_m3, but represents the most recent NCBI annotations => use as-is  
  
## Use within R  
#### these bioconductor annotation files have been used in ArchR package
#BSgenome  
library(BSgenome.Xtropicalis.Xenbase.xt10)  
genomeAnnotation <- createGenomeAnnotation(genome = BSgenome.Xtropicalis.Xenbase.xt10)  
  
#TxDb (specify path to file as necessary)  
library(AnnotationDbi)  
xt_TxDb <- loadDb("TxDb.Xtropicalis.Xenbase.xt10")  
  
#OrgDb
library(org.Xtropicalis.eg.db)  
xt_OrgDb <- org.Xtropicalis.eg.db  

geneAnnotation <- createGeneAnnotation(TxDb = xt_TxDb, OrgDb = xt_OrgDb)

