# VGG16-Face-Mask-Detection-
1. The dataset consists of three classes: "with_mask," "without_mask," and "not_proper_mask." Each class is represented by labels 0, 1, and 2, respectively.

2. The images are resized to a standard size of (224, 224) pixels to ensure compatibility with the VGG16 model and maintain uniformity.

3. To avoid bias during training, the data is shuffled and converted into arrays, which serve as input for the neural network.

4. The array data is normalized, scaling the pixel values to a standardized range typically between 0 and 1. Normalization enhances the model's performance by bringing features to a similar scale.

5. The VGG16 model, a deep convolutional neural network with 16 layers, serves as the base architecture for the face mask detection system in the CNN Architecture. VGG16 is renowned for its effectiveness in image classification tasks.

6. Although originally trained on the ImageNet dataset with over 1,000 classes, VGG16 is adapted for our  mask classification by modifying the last layer.

7. The last layer of the VGG16 model is replaced with a dense layer having three units, corresponding to the three classes: "with_mask," "without_mask," and "not_proper_mask." This modification enables the network to make predictions for face mask detection with multiple classes.

8. To prevent overfitting, two dropout layers are added after the dense layer.

9. The Adam optimizer is employed during the training process. Adam is an optimization algorithm that adaptively adjusts the learning rate and efficiently updates the model parameters.

10. For the loss function, Categorical Cross Entropy is utilized, as it is suitable for multi-class classification problems. It measures the dissimilarity between predicted and actual class labels.

11. Accuracy is evaluated using the formula: (True Positives + True Negatives) / (True Positives + True Negatives + False Positives + False Negatives). It provides insight into the model's ability to correctly classify instances across all three classes.

12. To enhance accuracy, a Haar cascade face classifier is integrated into the system. This classifier utilizes machine learning techniques to detect faces in an image
