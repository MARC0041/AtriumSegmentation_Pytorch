# AtriumSegmentation_Pytorch

## Todos:
- Move relevant ipynb files over
- Set up python conda environment
- Document setup


## Download nifti files
Document the steps for downloading the files, but due to large file sizes, gitignore them and simply record down the steps so it is reproducible

1. Download the files and expand the folder: https://drive.google.com/u/0/uc?id=1wEB2I6S6tQBVEPxir8cA5kFB8gTQadYY&export=download 
2. Place the files into this folder. "Task02_Heart" should have a json file, imagesTr, imagesTs, and labelsTr.
3. Add following lines to .gitignore 
```
*.nii.gz
Task02_Heart/dataset.json
*.npy
```

## Setup conda env
```
conda create --prefix ./pytorchatrium python=3.8
conda activate ./pytorchatrium

conda install numpy
conda install pandas -y
conda install matplotlib -y
conda install -c conda-forge tqdm
conda install dicom2nifti nibabel pydicom -y
conda install jupyter -y

<!-- make sure the kernel is visible on jupyter -->
python -m ipykernel install --user --name=pytorchatrium

<!-- conda install pytorch::pytorch torchvision torchaudio -c pytorch -y
conda install pandas numpy matplotlib -y
conda uninstall numpy
conda install numpy -->
```
*When running the notebook cell in vs code, it will prompt you to download the notebook package. 
*When python=3.9, there was an issue with import numpy. May also be because I installed pytorch first? 

At this stage you should be able to run the following import commands without issue:
```
import os
import sys
for p in sys.path:
    print(p)
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from pathlib import Path
from tqdm.notebook import tqdm 
import nibabel as nib
```
