# Dogs vs Cats - CNN Classifier

Classifies images of cats and dogs using a deep CNN.  

## Dataset
- Kaggle: [Dogs vs Cats Dataset](https://www.kaggle.com/datasets/princelv84/dogsvscats?resource=download)

## Model Architecture

```
Input: 3 x 256 x 256 RGB image

[Conv2d(3,32,3)] → BatchNorm2d(32) → ReLU → MaxPool2d(2)
[Conv2d(32,64,3)] → BatchNorm2d(64) → ReLU → MaxPool2d(2)
[Conv2d(64,128,3)] → BatchNorm2d(128) → ReLU → MaxPool2d(2)
Flatten
[Linear(128*30*30, 256)] → ReLU → Dropout(0.5)
[Linear(256, 64)]       → ReLU → Dropout(0.3)
[Linear(64, 1)]         → Sigmoid
