# Abstract

In recent years, single-cell RNA sequencing (scRNA-seq) technologies have revolutionised our understanding of cellular heterogeneity. Various methods have been developed to interpret this complexity, with Seurat and scVI emerging as prominent tools for scRNA-seq data clustering. This analysis gives insight into the differences in functionality and results of both methods. This is done by exploring the workflow of primarily scVI with relevant mentions of the Seurat workflow. The result of both workflows is a UMAP, which comes from the clustering of the data. 

# Project Dependencies

This project requires several Python packages which are listed in the `requirements.txt` file. 
You can install these dependencies using the following command:

```
pip install -r requirements.txt
```

## PyTorch Installation

Note that the `requirements.txt` does not include a version of PyTorch, you must install a different version depending on your system and whether you are utilising CPUs or GPUs.

Please visit the official PyTorch installation guide to find the command that is appropriate for your environment:

[PyTorch Installation Guide](https://pytorch.org/get-started/locally/)

Follow the instructions on the website to install the correct version of PyTorch for your system.

## Note for NVIDIA GPU Users

If you plan to use an NVIDIA GPU, ensure that you have the correct version of CUDA installed that is compatible with the PyTorch version you are installing. The PyTorch installation guide linked above provides information about which CUDA version is required for each PyTorch version.


# Workflow Prerequisites

To conduct the analysis presented in this project, you will need a Seurat `.h5ad` file. This file format is specifically designed for single-cell genomics data and is used to store the output of the Seurat workflow.

You can download the necessary `.h5ad` file and the original Seurat workflow from the following Google Drive location:

[Seurat `.h5ad` file and Workflow](https://drive.google.com/drive/folders/1_qHpi0s9k8x54v2LVw6mtNl2ylpWUx2j?usp=sharing)

Please ensure you have the correct permissions to access this data and download the file to your local environment before proceeding with the analysis.

# How to Run

## Prerequisites

Before proceeding, ensure you have Jupyter Notebook installed on your system. Jupyter Notebook is essential for running and interacting with the analysis scripts. If you do not have Jupyter Notebook installed, please visit [the official Jupyter installation guide](https://jupyter.org/install) for instructions.

## Setting Up the Data

After downloading the `.h5ad` file, place it in the designated `/h5ad/seurat/` directory of this project.

## Running the Analysis

Follow the instructions provided in the subsequent sections to run the analysis with the Seurat and scVI tools, and to compare their respective UMAP results.

## Customising Hyperparameters

To train the model with bespoke hyperparameters, alter the `train_params` variable in the script. Change `train_params = False` to `train_params = True` and modify the hyperparameter grid to suit your requirements.

For example, to adjust the settings, you would amend the grid parameters as follows:

```python
train_params = True
param_grid = {'n_hidden': [your_params], 'n_latent': range(your_params), 'n_layers': range(your_params)}
```
Please be aware that the hyperparameters: 
```python
param_grid = {'n_hidden': [128], 'n_latent': range(2, 51, 1), 'n_layers': range(1, 6, 1)}
```
have already been executed, and the outcomes are stored in the hp_models directory.

## Creating Additional UMAP Visualisations

If you wish to create other UMAP visualisations based on different model files, you need to modify the model variable in the script. For instance, to analyse different sets of hyperparameters, change the models list to include the corresponding model names, like so:
```python
model_dir = os.path.join(save_dir, "hp_model/")
models = ["1_128_2", "1_128_10", "1_128_20", "Your model names here"]
```
This will allow the script to generate UMAP visualisations for each specified model configuration.

This addition guides users on how to generate UMAP visualizations for different model configurations, making the markdown document more comprehensive for diverse use cases.


# Original Seurat Workflow

For those interested in the original Seurat workflow used to generate the `.h5ad` file, you can also find this in the Google Drive folder linked above. It may provide additional context and understanding of how the initial data was processed and analysed.

# Contact

If you encounter any issues accessing the data or have questions regarding the workflow, please feel free to reach out using the contact information provided below.

mghuibregtse@gmail.com

jaimymohammadi@gmail.com

