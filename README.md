# CELA1 Mediates Progressive Emphysema in Alpha-1 Antitrypsin Deficiency
 Data analysis of the proteomics for the paper by Andrew Devine et al.

Please let us know if you need any assistance in executing or understanding this code.

This repository contains the details of the LC-MS/MS data analysis for the paper titled : “CELA1 Mediates Progressive Emphysema in Alpha-1 Antitrypsin Deficiency"

The R markdown and the knitR html report are located in the main folder of the repository

All required files for the analysis are located in the folder 01_source_files

All the files generated during the data analysis are located in the folder 03_Output_files.

Note that you can install [RomicsProcessor](https://github.com/PNNL-Comp-Mass-Spec/RomicsProcessor) on its dedicated repository.

Raw files are deposited on [MassIVE](https://massive.ucsd.edu/ProteoSAFe/static/massive.jsp)

# Code requirements

The code was run using [R](https://cloud.r-project.org) v.4.2.1 on [Rstudio](https://rstudio.com) version 2022.07.1+554 for macOS.

Running the code require:

- The installation of [Devtools](https://cran.r-project.org/web/packages/devtools/index.html)

- The package[RomicsProcessor v.1.0.0](https://github.com/PNNL-Comp-Mass-Spec/RomicsProcessor/blob/master/RomicsProcessor_1.0.0.tar.gz) (follow the package page for installation instructions). RomicsProcessor is an R package that can be used to analyze omics data. The package provides a structured R object to store the data, allowing for reproducible data analysis. The package also supports creating analytically pipelines from previously processed objects and applying these pipeline to other objects. This allows for rapid development and reuse of bioinformatics methods.

- To run the code create a copy of the repository in a folder on your computer and open the file named "02 - Code.Rmd" and in the rmd file change the working directory on line 17

- The version of the different dependencies that were employed at time of analysis are contained in the "romics_proteins.rda" object located in the folder ".*/03 - Output files". After loading the object in the R environment you can get the version of all packages by typing the following in the R console
```
romics_proteins$dependencies

```

# Data pre-processing

The data was pre-processed using MaxQuant (v1.6.0.16) the file [parameters.txt](https://github.com/GeremyClair/The_influence_of_the_pulmonary_microenvironment_on_macrophage_and_T_cell_dynamics./blob/main/01_source_files/parameters.txt) generated by MaxQuant is provided. The [summary.txt](https://github.com/GeremyClair/The_influence_of_the_pulmonary_microenvironment_on_macrophage_and_T_cell_dynamics./blob/main/01_source_files/summary.txt) file indicates what raw files located on MassIVE were used for the analysis. The [peptide.txt](https://github.com/GeremyClair/The_influence_of_the_pulmonary_microenvironment_on_macrophage_and_T_cell_dynamics./blob/main/01_source_files/peptides.txt) and [proteinGroups.txt](https://github.com/GeremyClair/The_influence_of_the_pulmonary_microenvironment_on_macrophage_and_T_cell_dynamics./blob/main/01_source_files/proteinGroups.txt) files are also provided along with the metainformation of associated with the samples in the file [metadata.csv](https://github.com/GeremyClair/Effect_of_glomerular_disease_on_the_podocyte_cell_cycle/blob/main/01_Source_files/metadata.csv).
It is important to note that the [fasta](https://github.com/GeremyClair/The_influence_of_the_pulmonary_microenvironment_on_macrophage_and_T_cell_dynamics./blob/main/01_source_files/Uniprot_Mus_musculus_proteome_UP000000589_2021_06_28.fasta) file uploaded was the one used for the search.


The [R markdown knitR report file](https://github.com/GeremyClair/The_influence_of_the_pulmonary_microenvironment_on_macrophage_and_T_cell_dynamics./blob/main/02_code_Cela1.html) final report can be seen directly without having to run the code.

All the files generated during the data analysis are located in the folder 03 - Output files.


Please let us know if you need any assistance in executing or understanding this code.

## Contacts

Written by @GeremyClair for the Department of Energy (PNNL, Richland, WA) \
E-mail: geremy.clair@pnnl.gov or proteomics@pnnl.gov \
Website: https://omics.pnl.gov/ 

## License

This code is licensed under the 2-Clause BSD License; 
you may not use this file except in compliance with the License.  You may obtain 
a copy of the License at https://opensource.org/licenses/BSD-2-Clause

Copyright 2022 Battelle Memorial Institute