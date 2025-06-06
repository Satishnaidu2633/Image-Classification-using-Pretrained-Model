# 🫘 Bean Leaf Disease Classification using Pretrained GoogLeNet

This project focuses on classifying **bean plant leaves** into three categories using a pretrained deep learning model—**GoogLeNet**. It demonstrates the use of transfer learning for agricultural disease detection, specifically identifying leaf conditions such as:

- **Healthy**
- **Angular Leaf Spot**
- **Bean Rust**

## 📁 Dataset

The dataset contains images of bean leaves, categorized into three classes:

Each image is labeled and stored in its respective class directory. The dataset is loaded using `torchvision.datasets.ImageFolder`.

> **Note**: The dataset used is [Bean Leaf Disease Dataset](https://www.kaggle.com/datasets/emmarex/plantdisease) from Kaggle (if applicable).

## 🧠 Model Used

- **GoogLeNet (Inception v1)** from `torchvision.models`
- Transfer learning: Pretrained weights from ImageNet
- Final classifier layers adjusted for 3-class output

## ⚙️ Features

- Image transformations and augmentation using `torchvision.transforms`
- Training and validation loops using PyTorch
- Accuracy evaluation
- GPU support for faster training (if available)

## 🚀 How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/bean-leaf-disease-classification.git
    cd bean-leaf-disease-classification
    ```

2. Install dependencies:
    ```bash
    pip install torch torchvision matplotlib
    ```

3. Place the dataset as described above.

4. Launch the notebook:
    ```bash
    jupyter notebook "Image Classification using pretrained model.ipynb"
    ```

## 📊 Evaluation Metric

Model performance is measured using classification accuracy on the test dataset:

```python
test_accuracy = round((total_acc_test / len(test_dataset)) * 100, 2)
