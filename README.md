# ATTENTION! Work in progres -- will be finished soon
# I plan to update all the scripts and store at github unzipped

# Reproducibility materials for the paper
>Kashnitsky, I., Beer, J. de, & Wissen, L. van. (2017). Decomposition of regional convergence in population aging across Europe. Genus, 73(1), 2. https://doi.org/10.1186/s41118-017-0018-2

## REQUIREMENTS AND PRELIMINARY NOTES 
The analysis and the necessary data preparation were conducted using R, a language and environment for statistical computing, version 3.2.4 [https://cran.r-project.org/]. 
A valid internet connection is necessary. To ensure full reproducibility of the analysis, i.e. proper execution of each R script, all the required R packages will be downloaded in the versions of 2016-03-14. For this reason we use R package for reproducible research called "checkpoint". Also, to replicate the results of the analysis, the requited data have to be downloaded; thus, you will need a valid internet connection. About 35MB of data will be downloaded.
It is recommended (but not obligatory) to use RStudio (IDE for R) [the used version is 0.99.892, https://www.rstudio.com/products/rstudio/download/], and open the project file (2016_Genus_Kashnitsky.Rproj). Then, there is no need to set working directory, as the R project recognizes relative paths. If, for some reason, you prefer not to use RStudio, working directory should be set to the top-level parental folder (2016_Genus_Kashnitsky). 
Each time a fresh R session is started, the preparation steps should be taken: 
1) working directory set to the top-level parental folder (2016_Genus_Kashnitsky) [not necessary if you use RStudio and open the project file (2016_Genus_Kashnitsky.Rproj)]; 
2) required packages loaded (script "R_scripts/1_preparation/1.01_install_required_packages.R"); 
3) and self-written functions loaded ("R_scripts/1_preparation/1.02_load_own_functions.R").

## REPLICATION. HOW TO
1. Unzip the archive into any directory.
2. Open "2016_Genus_Kashnitsky.Rproj" file in the main project directory.
3. Run the "R_scripts/master_script.R" file. 
Wait. That's it.
The results are stored in the directory "_output".

## LOGIC OF THE PROCESS
The whole process is split into three parts, which is reflected in the structure of R scripts. First, the steps required for reproducibility are taken. Second, all data manipulations and calculations are performed. Finally, at the third step, the analysis is done, and the outputs are stored in "_output" directory. 
The names of the scripts are quite indicative, and each script is reasonably commented. 

## CONTENTS OF THE REPRODUCIBILITY PACKAGE
Directories and sub-directories in alphabetical order.  
= "_output" the results are stored here  
= "data0_supplementary"  
=== "EU_nuts" NUTS-2 classification for EU-28, version 2010  
= "data1_raw" raw data downloaded here  
=== "Eurostat" official data from Eurostat  
===== "observed" data for the observed period, 2003-2012  
===== "projected" projected data, EUROPOP2013 regional, 2013-2042  
=== "Missing_data" data from national statistical offices and HMD needed to fill the missings and harmonize the data (sub-directories will appear after the execution of script "2.04_missing_download&unzip.R")  
===== "raw_DE" data for Germany  
===== "raw_DK" data for Denmark  
===== "raw_SI" data for Slovenia  
= "data2_prepared" prepared for the analysis raw data  
= "data3_calculated" ready for the analysis and visualization data are stored here  
= "geo_data" spatial objects prepared for R, needed to map the results  
= "R_packages" a directory where the package "checkpoint" and its dependences will be installed  
=== ".checkpoint" directory for all other required packages, handled by "checkpoint"  package in a reproducible way.  
= "R_scripts"  
=== "0_own_finctions"  
=== "1_preparation"  
=== "2_data_manipulation"  
=== "3_analysis"  
=== "master_script.R" - !!! this is the main script to be run !!!  
= "2016_Genus_Kashnitsky.Rproj" RStudio project file  
