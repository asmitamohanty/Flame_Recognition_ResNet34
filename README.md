# Flame_Recognition_ResNet34
Goal of this project is to classify different burning liquids (flames) using CNN-based approach through transfer learning of Resnet-34. 

# Dataset
Burning liquid dataset is downloaded from https://doi.org/10.1007/s10973-021-10903-2 – Supplementary Information, File #2. The dataset consists of 3000 hi-resolution flame images of burning ethanol, pentane, and propanol.

# Data Augmentation
The dataset is organized into train, validation, and test sets with a split ratio of 70%, 15%, and 15% respectively. Images are preprocessed with normalization and augmentation techniques such as rotations, flips, and scaling.

# Model
A pretrained ResNet34 CNN model is used where the fully connected layer's output is modified to output predictions of 3 flame categories.
The model is trained using the Adam optimizer with a learning rate of 1e-4 for 15 epochs. During training, the model's performance is evaluated on both the training and validation sets. Adjusted layer freezing and learning rate experiments are conducted for potential performance improvements.

# Results
After training, the model achieves an accuracy of 99.5% on the validation set.

# Layer Visualization
Visualization of intermediate layers of the model is provided for better understanding of feature extraction

# Analysis
- Observed accuracy & learning curvers are reaching plateaus in just fewer epochs only when we unfreeze more layers
- A comparison is made with the baseline with the observation that the fine-tuned model with unfreezing layers is achieving better accuracy
