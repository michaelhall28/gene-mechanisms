
This repository contains Jupyter Notebooks for generating the figures in Hall et al. Mutations observed in somatic evolution reveal underlying gene mechanisms


## Software Requirements
-python 3

-darwinian_shift code available from https://github.com/michaelhall28/darwinian_shift  
Follow the instructions on that repository to install the code and download the required reference files for GRCh37. 
If installing the minimal dependencies, the packages FreeSASA and PyBigWig must be installed in addition.  

-Other python packages required to run the notebooks are create all plots:
- jupyter
- seaborn


## Data requirements
Most data files required to run the notebooks are included in the repository. However there are two large files that have to be downloaded separately: 

To run the NOTCH1_transmembrane notebook a BigWig file of Phylop conservation scores is required. This file can be downloaded through the UCSC genome browser here: http://hgdownload.soe.ucsc.edu/goldenPath/hg19/phyloP100way/hg19.100way.phyloP100way.bw   
Warning - this file is approximately 9Gb.  

To run the analysis of _PIK3CA_ mutations overlapping with ClinVar, the ClinVar variant_summary.txt file is required. This can be downloaded from the ClinVar FTP site (https://ftp.ncbi.nlm.nih.gov/pub/clinvar/). Once uncompressed, the file is approximately 1.3Gb.  
The file we used was downloaded 7th April 2020.  

In addition, to run the analysis of misfolding mutations in mouse proteins, a folder of CSV files must be created. See the Supplementary Methods, and the notebook `FoldX vs nonsense-Mouse.ipynb` explains the required file format. 

***

The human somatic mutation data from both the oesophagus and skin is included in the repository. These were downloaded from the original studies:  

The mutation data from normal oesophagus data came from Martincorena et al. Somatic mutant clones colonize the human esophagus with age. Science. 2018. 
The data used is in Supplementary Table 2 (https://science.sciencemag.org/highwire/filestream/716966/field_highwire_adjunct_files/2/aau3879_TableS2.xlsx)

The mutation data from normal skin come from Fowler et al. Selection of Oncogenic Mutant Clones in Normal Human Skin Varies with Body Site, Cancer Discovery, 2021. 
The mutation data used is in Table S4 (https://aacrjournals.org/cancerdiscovery/article/11/2/340/3261/Selection-of-Oncogenic-Mutant-Clones-in-Normal#supplementary-data). 
In addition, a full list of dN/dS results was created by running the R package dndscv on this dataset.  


The mouse mutation data can be downloaded from Colom et al 2020 https://www.nature.com/articles/s41588-020-0624-3. 


## Notebooks 

`calculating_spectra.ipynb` contains the code to create the `skin_trinuc_spectrum.txt` and `oesophagus_trinuc_spectrum.txt` files used as input for the other notebooks.  
All of the other notebooks recreate figures from the paper. 

