# Image Classification using Pretrained Model (GoogLeNet)

This project demonstrates how to perform image classification using a pretrained deep learning model—**GoogLeNet**—on a custom dataset. The model is fine-tuned to classify images into different categories, showcasing the power of transfer learning in computer vision.

## 📂 Project Structure

- `Image Classification using pretrained model.ipynb`: Main Jupyter notebook containing code for loading data, training, and evaluating the model.
- `data/`: Folder containing training and testing image datasets (not included in this repository).
- `models/`: (Optional) Directory to save trained model weights.

## 🧠 Model Used

- **GoogLeNet (Inception v1)**: A deep convolutional neural network that achieved top results in the ImageNet challenge. It is used here as a pretrained model with fine-tuning on a specific image dataset.

## 🔍 Features

- Pretrained GoogLeNet model from `torchvision.models`
- Custom dataset loading with PyTorch `ImageFolder`
- Train-test split and DataLoader preparation
- Accuracy evaluation on test dataset
- `torch.no_grad()` used for inference efficiency

## 🚀 How to Run

1. Clone this repository:
    ```bash
    git clone https://github.com/Satishnaidu2633/Image-Classification-using-Pretrained-Model
    cd image-classification-googlenet
    ```

2. Install required libraries:
    ```bash
    pip install torch torchvision matplotlib
    ```

3. Place your image dataset in a folder structure like:
    ```
    data/
      train/
        class1/
        class2/
        ...
      test/
        class1/
        class2/
        ...
    ```

4. Open the Google Colab and run all cells:
    ```bash
    google colab "Image Classification using pretrained model.ipynb"
    ```

## 📊 Evaluation

The model is evaluated using accuracy metric calculated on the test dataset:
```python
test_accuracy = round((total_acc_test / len(test_dataset)) * 100, 2)
