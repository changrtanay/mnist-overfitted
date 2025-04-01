# MNIST Image Digit Recognition

This project implements an image digit recognition task using the MNIST dataset. The goal is to train a model on the dataset, intentionally make it overfit, and then apply techniques to mitigate overfitting while keeping the same architecture.

## Dataset
The MNIST dataset consists of 60,000 training images and 10,000 test images of handwritten digits (0-9). Each image is grayscale and has a size of 28x28 pixels.

## Implementation Details
1. **Data Preprocessing:**
   - Load the MNIST dataset.
   - Normalize the pixel values to the range [0,1].
   - Split the training set into 50,000 training and 10,000 validation samples.

2. **Overfitting Model:**
   - several dense layers.
   - High-capacity architecture is used to force overfitting.
   - The model is trained for 20 epochs.

3. **Mitigating Overfitting:**
   - Dropout layers are added to reduce overfitting.
   - The same architecture is retained while introducing dropout regularization.
   - The model is trained again for 20 epochs.

4. **Evaluation:**
   - The model is evaluated on the test set to measure accuracy.

## Requirements
Ensure you have the following dependencies installed before running the script:
```bash
pip install tensorflow numpy matplotlib
```

## Running the Script
Run the Python script using:
```bash
python mnist_overfitted.py
```

## Expected Results
- The first training phase will likely show a high validation loss, indicating overfitting.
- After applying dropout, the model should generalize better, improving test accuracy.

