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
```

## Setup conda env
```
conda create --prefix ./pytorch_arm64_atrium python=3.9
conda activate ./pytorch_arm64_atrium

conda install pytorch::pytorch torchvision torchaudio -c pytorch -y
```