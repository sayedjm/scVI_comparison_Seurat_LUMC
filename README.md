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
