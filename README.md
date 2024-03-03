# Brain Tumor Classification with Deep Learning

## Overview
This GitHub repository contains code for a brain tumor classification project using deep learning, implemented with Keras and TensorFlow. The primary goal is to develop a model capable of distinguishing between tumorous and non-tumorous brain images.

## Problems Faced and Solutions

### 1. Data Renaming
**Issue:** The original dataset files lacked a consistent naming convention.

**Solution:** Renamed the files in the 'yes' and 'no' directories to ensure consistency. Images in the 'yes' directory were prefixed with "Y_" and in the 'no' directory with "N_".

### 2. Data Imbalance
**Issue:** The number of tumorous and non-tumorous images were imbalanced.

**Solution:** Implemented data augmentation using the ImageDataGenerator from Keras to artificially increase the number of images in the minority class.

### 3. Image Preprocessing
**Issue:** Raw images needed preprocessing steps before feeding them to the model.

**Solution:** Applied a series of preprocessing steps, including converting images to grayscale, applying GaussianBlur, thresholding, erosion, and dilation to enhance tumor features.

### 4. Data Splitting
**Issue:** Needed to split the data into training, testing, and validation sets.

**Solution:** Created directories for each set and moved the augmented images accordingly, maintaining an 80% - 10% - 10% split.

### 5. Model Building
**Issue:** Implemented a VGG19-based model with a frozen convolutional base, but initial performance was suboptimal.

**Solution:** Gradually unfroze layers of the convolutional base and fine-tuned the model to improve performance.

### 6. Training and Evaluation
**Issue:** Initial training didn't achieve desired accuracy.

**Solution:** Utilized early stopping, model checkpointing, and learning rate reduction callbacks. Also, evaluated the model on the test and validation sets.

### 7. Model Comparison
**Issue:** Model performance varied during different stages of training.

**Solution:** Saved model weights at various stages and compared their performance to choose the best one.

## Results
The final model achieved a validation accuracy of approximately 81% and a testing accuracy of around 57%.

## Usage
1. Download the brain tumor dataset.
2. Run the provided code to preprocess, augment, and train the model.
3. Evaluate the model on new data.

Feel free to explore and contribute to further improve the classification accuracy and robustness of the model.
