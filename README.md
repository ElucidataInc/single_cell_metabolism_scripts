# Analysis scripts for the publication 
# **Inferring metabolic rewiring in embryonic neural development using single cell data**


### Scripts

- E135_Analysis.ipynb - Seurat Analysis using E13.5 data from GSE107122
- E155_Analysis.ipynb - Seurat Analysis using E15.5 data from GSE107122
- E175_Analysis.ipynb - Seurat Analysis using E17.5 data from GSE107122
- E175_E135_CCA.ipynb - Canonical correlation analysis for combining E13.5 and E17.5 data
- metabolic_state_all_days.ipynb - Analysis for identifying metabolic states in E13.5, E15.5 and E17.5 datasets.
- GSEA_RPsvsNeurons.ipynb - GSEA Analysis between RPs and Neurons, and between state S0 and state S2 cells for E13.5, E15.5, E17.5 datasets
- heatmap_all_days.ipynb - Heatmap for average gene expressions of all genes for RPs and Neurons in  E13.5, E15.5 and E17.5 datasets.
- Random_genes_state_cell_overlap.ipynb - Analysis for Random gene set sampling, state extraction using random genes and comparing cell type overlap with metabolic states.
- DentateGyrusAnalysis.ipynb - Seurat Analysis using dentate gyrus data from GSE104323 


### Setting up Seurat v2
Multiple analysis were done using Seurat v2

In an R console
```
install.packages("R.utils")
system("wget https://cran.r-project.org/src/contrib/Archive/SDMTools/SDMTools_1.1-221.2.tar.gz")
install.packages("SDMTools_1.1-221.2.tar.gz")
devtools::install_version(package = 'Seurat', version = package_version('2.3.0'))
```

Install jre for Seurat clustering
```
$ sudo apt install default-jre
```

### Other R packages 
```
install.packages(c("GSA","ggsci"))
BiocManager::install("fgsea")
BiocManager::install("cmapR")
```

### CombiT Algorithm was run using [Polly IntOmix](https://resources.elucidata.io/intomix) 