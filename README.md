# Performances of Deep Learning Models on the Stanford Dogs Dataset

This repository stores a collection of deep learning model training Google Colab notebooks. The models are trained on the Stanfords Dog dataset for the dog breed fine-grained classification problem.

## Model Training
All models are developed on Google Colab and trained with a single GPU. The training was performed with transfer learning technique, where the model is formed by a state-of-the-art deep learning model pretrained on ImageNet with a new classification block attached. The train-validation-test split is 80-10-10.

The training process consists of two phases: 
### 1. Feature extraction
* All pretrained weights are frozen
* Learning rate: 1e-2 (1e-3 for ViT)

### 2. Fine-tuning
* All weights in the model are unfrozen
* Learning rate: 1e-5

The Adam optimizer and an early stopping criteria with 5 epochs of tolerance are applied in both phases.

## Model Performances
|Model|Test Accuracy|Test Top-5 Accuracy|Size(MB)|Parameters(M)|Link to Final Model|
|:---   | :---: |:---: |:---: |:---: |:---: |
|MobileNetV2|79.30%|97.12%|14|3.5|[Keras h5](https://drive.google.com/file/d/1-1QRmYuGClWCIzo6l4yUwImkZ-0CuzLD/view?usp=sharing)|
|DenseNet121|80.57%|98.10%|33|8.1|[Keras h5](https://drive.google.com/file/d/1-wY0G44HG5JmdbJ9Y_BZN8bWq350VQ7p/view?usp=sharing)|
|EfficientNetB0|82.96%|97.90%|29|5.3|[Keras h5](https://drive.google.com/file/d/1-y6MP9vumLvdBLR7oaMWkVgIT19lNZKh/view?usp=sharing)|
|EfficientNetV2B0|86.62%|98.73%|29|7.2|[Keras h5](https://drive.google.com/file/d/1-0Lv1QeRTFE7ib1G2Erz4_t5kgOb9ta9/view?usp=sharing)|
|EfficientNetV2B1|87.65%|87.65%|34|8.2|[Keras h5](https://drive.google.com/file/d/1-38BYFkVBnAzahI2naZnwaTFXcAmbP6v/view?usp=sharing)|
|EfficientNetV2B2|89.70%|99.22%|42|10.2|[Keras h5](https://drive.google.com/file/d/1-QdEzFdRRmXOZEcenNIgPhi6ZpYVPsU2/view?usp=sharing)|
|EfficientNetV2B3|92.14%|99.56%|59|14.5|[Keras h5](https://drive.google.com/file/d/1-TU2kCHDXWVyuyVN7z7rOjGTwY8d7QaH/view?usp=sharing)|
|EfficientNetV2S|90.43%|98.93%|88|21.6|[Keras h5](https://drive.google.com/file/d/106Ag7tarebY2yHpDzQq2JiiLl1JjHraa/view?usp=sharing)|
|ResNet50V2|74.32%|94.24%|98|25.6|[Keras h5](https://drive.google.com/file/d/1-GEjKCn_teBjnt3I0RsHwG9fj2r1CMR5/view?usp=sharing)|
|InceptionResNetV2|86.04%|98.39%|215|55.9|[Keras h5](https://drive.google.com/file/d/1-F_0UlhV2vnchfhtoyjXtbmTbfJ_iALi/view?usp=sharing)|
|ViT|93.20%|99.56%|330|86|[PyTorch pt](https://drive.google.com/file/d/1-iRf_hn632MF3-TCni1Fc6dsbH9I0jhS/view?usp=sharing), [Hugging Face](https://huggingface.co/skyau/dog-breed-classifier-vit)|

## Instructions for Running the Training Notebooks
After pip installing all required libraries, the runtime has to be restarted once before importing the libraries. 
