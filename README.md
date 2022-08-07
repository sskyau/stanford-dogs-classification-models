# Performances of Deep Learning Models on the Stanford Dogs Dataset

This repository stores a collection of deep learning model training Google Colab notebooks. The models are trained on the Stanfords Dog dataset for the dog breed fine-grained classification problem.

## Model Training
The training was performed with transfer learning technique, where the model is formed by a state-of-the-art deep learning model pretrained on ImageNet with a new classification block attached. The train-validation-test split is 80-10-10.

The training process consists of two phases: 
### 1. Feature extraction
* All pretrained weights are frozen
* Learning rate: 1e-2

### 2. Fine-tuning
* All weights in the model are unfrozen
* Learning rate: 1e-5

The Adam optimizer and an early stopping criteria with 5 epochs of tolerance are applied in both phases.

## Model Performances
|Model|Test Accuracy|Size(MB)|Parameters(M)|
|:---   | :---: |:---: |:---: |
|MobileNetV2|79.30%|14|3.5|
|DenseNet121|80.57%|33|8.1|
|EfficientNetB0|82.96%|29|5.3|
|EfficientNetV2B0|86.62%|29|7.2|
|EfficientNetV2B1||34|8.2|
|EfficientNetV2B2||42|10.2|
|EfficientNetV2B3||59|14.5|
|EfficientNetV2S||88|21.6|
|ResNet50V2||98|25.6|
|InceptionResNetV2||215|55.9|
|ViT||346|86|
