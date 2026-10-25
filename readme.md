# CNN Flower Image Classification

## Project Overview

This project implements a Convolutional Neural Network (CNN) using TensorFlow and Keras to classify flower images into five categories. The model learns visual patterns from flower images and predicts the corresponding flower category.

## Problem Statement

A horticulture company wants to automate flower identification using deep learning. This project builds a CNN-based image classification model to identify five types of flowers.

## Dataset

The project uses the TensorFlow Flower Photos dataset.

**Dataset URL:** https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz

The dataset contains five flower classes:

- Daisy
- Dandelion
- Roses
- Sunflowers
- Tulips

Images are resized to 180 × 180 pixels and split into training and validation datasets.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Model Architecture

The CNN architecture includes:

1. Input layer for 180 × 180 RGB images
2. Convolutional layers with ReLU activation
3. Max pooling layers
4. Global average pooling or flattening, depending on the final model architecture
5. Fully connected Dense layer with ReLU activation
6. Dropout for regularization
7. Output Dense layer with Softmax activation for five-class classification

The model is compiled using the Adam optimizer and sparse categorical cross-entropy loss.

## Project Structure

```text
CNN_Image_Classification/
│
├── dataset/
│   └── flower_photos/
│       ├── daisy/
│       ├── dandelion/
│       ├── roses/
│       ├── sunflowers/
│       └── tulips/
│
├── cnn_model.ipynb
├── trained_model.h5
├── requirements.txt
├── README.md
│
└── output_images/
    ├── accuracy_curve.png
    ├── loss_curve.png
    ├── confusion_matrix.png
    └── sample_predictions.png
```

## Installation

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd CNN_Image_Classification
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual GitHub repository URL.

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the notebook

Open Jupyter Notebook:

```bash
jupyter notebook
```

Then open `cnn_model.ipynb` and execute the cells in order.

## Model Training

The model is trained using the flower image dataset. Data augmentation and dropout are used to help reduce overfitting. Early stopping and learning-rate reduction callbacks help manage the training process.

The trained model is saved as:

```text
trained_model.h5
```

## Model Evaluation

The model is evaluated using:

- Training accuracy
- Validation accuracy
- Training and validation loss
- Classification report
- Confusion matrix
- Sample flower predictions

The generated graphs and prediction visualizations are saved in the `output_images/` directory.

## Results and Observations

The initial training results showed high training accuracy compared with validation accuracy, indicating possible overfitting. Further improvements may be achieved through data augmentation, hyperparameter tuning, additional training data, and transfer learning.

**Final validation accuracy:** Add the value from your final training results.

**Best validation accuracy:** Add the best validation accuracy recorded during training.

## Future Improvements

- Apply transfer learning using MobileNetV2 or EfficientNet.
- Tune the learning rate and batch size.
- Increase training-data diversity.
- Improve generalization with regularization and data augmentation.
- Evaluate class-wise performance and investigate misclassified images.

## Conclusion

This project demonstrates how a CNN can be developed and evaluated for five-class flower image classification using TensorFlow and Keras. The project includes image preprocessing, model training, performance evaluation, prediction visualization, and suggestions for improving generalization.

## Author

Karthik D

## License

The dataset is provided by TensorFlow's example images repository. Review the dataset's accompanying license before redistributing the images.