# Abstract

In recent years, single-cell RNA sequencing (scRNA-seq) technologies have revolutionised our understanding of cellular heterogeneity. Various methods have been developed to interpret this complexity, with Seurat and scVI emerging as prominent tools for scRNA-seq data clustering. This analysis gives insight into the differences in functionality and results of both methods. This is done by exploring the workflow of primarily scVI with relevant mentions of the Seurat workflow. The result of both workflows is a UMAP, which comes from the clustering of the data. Because of this, the difference in UMAPs is completely the result of the different methods used. Seurat uses principal component analysis (PCA) to cluster its data. This is not the case with scVI because it uses variational autoencoders (VAE) to cluster its data, which does not work with normalised data. VAE is a generative model that can identify non-linear patterns and is therefore more applicable to larger and more complex datasets instead of the linear algorithm PCA. The resulting UMAPs give an accurate representation of the clustering and use the lower dimensionality representation to showcase these cell clusters. Both UMAPs are based on the Louvain algorithm to identify the different cell types. This does result in both UMAPs containing 6 cell types, but the resulting types and the clusters differ. scVI creates a more informative and representative UMAP than Seurat based on the fact that it shows a clearer division between clusters and cell types. Furthermore, scVI identifies clusters more accurately based on expected biological results than Seurat. The differences can further be seen in the marker genes identified by both workflows.

# Project Dependencies

This project requires several Python packages which are listed in the `requirements.txt` file. 
You can install these dependencies using the following command:

```
pip install -r requirements.txt
```

## PyTorch Installation

Note that the `requirements.txt` does not include a version of PyTorch, you must install a different version depending on your system and whether you are utilizing CPUs or GPUs.

Please visit the official PyTorch installation guide to find the command that is appropriate for your environment:

[PyTorch Installation Guide](https://pytorch.org/get-started/locally/)

Follow the instructions on the website to install the correct version of PyTorch for your system.

## Note for NVIDIA GPU Users

If you plan to use an NVIDIA GPU, ensure that you have the correct version of CUDA installed that is compatible with the PyTorch version you are installing. The PyTorch installation guide linked above provides information about which CUDA version is required for each PyTorch version.
