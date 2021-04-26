## Description
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
Only once, at Linux prompt (specify path to file as necessary): R CMD INSTALL "BSgenome.Xtropicalis.Xenbase.xt10_0.1.tar.gz"  
## Use, within R
library(BSgenome.Xtropicalis.Xenbase.xt10)  
genomeAnnotation <- createGenomeAnnotation(genome = BSgenome.Xtropicalis.Xenbase.xt10)  

