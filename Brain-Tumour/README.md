Brain Tumor Detection using CNN

This code implements a Convolutional Neural Network (CNN) for binary classification of brain MRI images into Tumor or No Tumor. The workflow includes data loading, preprocessing, model building, training, evaluation, and prediction visualization.

Steps Involved

1. Import Libraries

tensorflow & keras: For building and training the CNN.

ImageDataGenerator: For loading and augmenting images.

matplotlib: For visualizing training results.

numpy & os: For array processing and file operations.

random: For selecting random images for prediction examples.

2. Paths for Dataset

train_dir and test_dir: Paths to training and testing datasets stored in Google Drive.

Dataset structure should have subfolders for each class (e.g., Tumor and No Tumor).

3. Data Preprocessing with Augmentation

train_datagen: Rescales pixel values and applies augmentations such as rotation, zoom, and flipping to make the model more robust.

validation_split=0.2: Reserves 20% of training data for validation.

test_datagen: Only rescales test images without augmentation.

4. Data Generators

train_generator: Loads training images in batches and applies augmentations.

val_generator: Loads validation images from training data.

test_generator: Loads testing images without augmentation.

5. Building the CNN Model

Convolutional Layers: Extract features from images (Conv2D).

Pooling Layers: Reduce spatial size and computation (MaxPooling2D).

Flatten Layer: Converts 2D features to a 1D vector.

Dense Layers: Perform classification.

Dropout Layer: Reduces overfitting by randomly dropping connections.

Output Layer: Single neuron with sigmoid activation for binary classification.

6. Model Compilation

Optimizer: Adam

Loss: Binary crossentropy (appropriate for two classes).

Metric: Accuracy.

7. Model Training

model.fit: Trains the model for 10 epochs, validating after each epoch.

8. Model Evaluation

model.evaluate: Computes loss and accuracy on test data.

9. Plotting Training Results

Plots accuracy and loss curves for training and validation datasets to visualize performance.

10. Prediction Example

Picks a random test image.

Processes and predicts whether the MRI shows a tumor or not.

Displays the image with the predicted label and probability.

Summary:
This script is a complete CNN pipeline for brain tumor detection — from data preparation to model evaluation and sample prediction. Augmentation helps improve model generalization, and visualization helps understand the learning process.
