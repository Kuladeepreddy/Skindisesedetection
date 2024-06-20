Skin Lesion Classification using CNN
Overview
This project develops a Convolutional Neural Network (CNN) to classify skin lesions using the HAM10000 dataset. The model is designed to distinguish between different types of skin lesions with high accuracy.

Dataset
Source: HAM10000
Images: High-resolution images of various skin lesions
Metadata: Information about the type of lesion, patient age, sex, and localization
Preprocessing
Resized images to 100x75 pixels
Normalized pixel values
Filled missing age values with the mean
Mapped lesion types to categorical indices
Model Architecture
Type: Sequential
Layers:
2 Conv2D layers (32 filters) with ReLU activation, Same padding
MaxPooling layer
Dropout layer (25%)
2 Conv2D layers (64 filters) with ReLU activation, Same padding
MaxPooling layer
Dropout layer (40%)
Flatten layer
Dense layer (128 neurons) with ReLU activation
Dropout layer (50%)
Output Dense layer (7 neurons) with softmax activation
Training
Optimizer: Adam
Loss Function: Categorical Crossentropy
Metrics: Accuracy
Augmentation: ImageDataGenerator for rotation, zoom, width/height shift
Callbacks: EarlyStopping, ReduceLROnPlateau
Evaluation
Split data into training, validation, and test sets
Evaluated model performance on validation and test sets
Saved the trained model to model_skin.h5
Results
Achieved high accuracy on validation and test sets
Prevented overfitting with data augmentation and regularization
