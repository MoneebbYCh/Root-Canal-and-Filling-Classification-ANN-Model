# Root-Canal-and-Filling-Classification-ANN-Model

This code implements an ANN model to classify medical images into two categories: "Root Canal" 
and "Filling."  

Data Loading and Preprocessing 
The function load_images_and_labels() loads images and their corresponding labels from two 
separate folders. It reads the images, resizes them to 128x128 pixels, and normalizes their pixel values 
to a range between 0 and 1. The labels are read from text files, with the first value indicating the class 
("Root Canal" or "Filling"). These labels are mapped to numeric values (0 for "Root Canal" and 1 for 
"Filling").  

Model Building 
The model is a Sequential neural network with the following layers: 
Flatten: Converts the image into a one-dimensional vector. 
Dense layers: Several fully connected layers with ReLU activation for learning complex patterns. 
Dropout layer: Helps prevent overfitting by randomly disabling neurons during training. 
Output layer: A single neuron with a sigmoid activation, providing a probability for the class 
prediction (0 for "Root Canal" and 1 for "Filling"). 

Model Training 
The model is compiled using the Adam optimizer and binary cross-entropy loss function. It is trained 
for 10 epochs using the training set, with validation performance checked using the validation set. 

Evaluation 
After training, the model makes predictions on the test set. The predictions are converted into binary 
outcomes (0 or 1) based on a 0.5 threshold. The accuracy of the model is computed, and a 
classification report is generated, showing precision, recall, and F1-score for each class.

![image](https://github.com/user-attachments/assets/a2e60333-67d5-4400-9e22-6bbfc4296ce0)

The model achieves a strong accuracy of 85.19% overall. It performs well on the "Root Canal" class, 
with a perfect recall of 1.00 and a solid F1-score of 0.92, indicating accurate and consistent 
predictions for this class.
