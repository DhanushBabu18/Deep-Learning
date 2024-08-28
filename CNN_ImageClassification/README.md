## Image Classification using Convolutional Neural Networks (CNN)
# Overview
This project focuses on image classification using Convolutional Neural Networks (CNNs) with the CIFAR-10 dataset. The CIFAR-10 dataset consists of 60,000 32x32 color images in 10 different classes, with 6,000 images per class. The dataset is split into 50,000 training images and 10,000 test images. The project explores building a CNN model to classify images into one of the 10 categories: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck.
### Project Objectives
1.Data Preprocessing: Normalize the pixel values to the range [0, 1] and reshape the labels for proper input to the model.

2.Model Building:
ANN: Initially, an Artificial Neural Network (ANN) model was implemented to classify the images, but the results were suboptimal.
CNN: A more sophisticated CNN model was then built, taking advantage of convolutional layers and pooling to capture spatial hierarchies in the data.

3.Training and Evaluation: Train both the ANN and CNN models, evaluate their performance on the test set, and compare the results.

4.Results: Analyze the model's accuracy and performance metrics such as precision, recall, and F1-score using the classification report.

### Dataset
The CIFAR-10 dataset is a well-known benchmark dataset in the field of machine learning and computer vision. It contains 60,000 color images in 10 classes, with 50,000 images for training and 10,000 for testing.
- **Classes**:
  - Airplane
  - Automobile
  - Bird
  - Cat
  - Deer
  - Dog
  - Frog
  - Horse
  - Ship
  - Truck
 
### Model Architecture
#### Artificial Neural Network (ANN)
**Layers**:
- Flatten Layer: Converts the 3D input (32x32x3) into a 1D vector.
- Dense Layer 1: 3000 neurons, ReLU activation.
- Dense Layer 2: 1000 neurons, ReLU activation.
- Output Layer: 10 neurons, Softmax activation.

**Optimizer:**  SGD

**Loss Function:**  Sparse Categorical Crossentropy

**Results:**  The ANN achieved an accuracy of approximately 48.2% on the test set, which was not satisfactory.
#### Convolutional Neural Network (CNN)
**Layers**:
- Conv2D Layer 1: 32 filters, kernel size (3x3), ReLU activation.
- MaxPooling Layer 1: Pool size (2x2).
-Conv2D Layer 2: 32 filters, kernel size (3x3), ReLU activation.
-MaxPooling Layer 2: Pool size (2x2).
- Flatten Layer: Converts the 3D input into a 1D vector.
- Dense Layer: 64 neurons, ReLU activation.
- 
**Output Layer**: 10 neurons, Softmax activation.
  
**Optimizer**: Adam

**Loss Function**: Sparse Categorical Crossentropy

**Results**: The CNN model significantly improved the classification performance, achieving an accuracy of approximately 68.0% on the test set.

