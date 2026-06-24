# Medical Image Classification using CNNs

## Project Overview

This project classifies MRI medical images using:

- Custom CNN models
- Transfer learning CNN models
- Explainable AI (Grad-CAM)


## Dataset

Dataset:
BraTS 2019

Classes:

- Tumor (Yes)
- No Tumor (No)


Dataset structure:

data/

└── raw/

    └── BraTS2019 dataset/

        ├── train/

        ├── valid/

        └── test/


## Environment Setup

Create virtual environment:

python -m venv .venv


Activate:

Windows:

.venv\Scripts\activate


Install requirements:

pip install -r requirements.txt



## Data Preparation

Place BraTS2019 dataset inside:

data/raw/


Run validation:

python scripts/data_validation.py


Run preprocessing:

python scripts/preprocessing.py



## Train Custom CNN Models


CNN3:

python -m training.train_custom


Models saved:

results/custom_models/



## Train Pretrained Models


MobileNetV2

SqueezeNet

ResNet18


Run:

python -m training.train_pretrained


Models saved:

results/pretrained_models/



## Evaluation


Custom CNN:

python -m training.evaluate_custom


Pretrained:

python -m training.evaluate_pretrained



## XAI Generation


Custom CNN Grad-CAM:

python -m xai.gradcam_custom



ResNet Grad-CAM:

python -m xai.gradcam_pretrained



Outputs:

results/xai/


## Git Workflow

After every task:

git add .

git commit -m "TaskX.Y: description"

git push