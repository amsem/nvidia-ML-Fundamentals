# Deep Learning Model for Fresh and Rotten Fruit Classification

This project demonstrates the development of a deep learning model for classifying fresh and rotten fruits. The model is trained on a dataset containing images of fresh and rotten apples, oranges, and bananas, sourced from Kaggle.

## Dataset

The dataset consists of six categories of fruits: fresh apples, fresh oranges, fresh bananas, rotten apples, rotten oranges, and rotten bananas. Each category contains a varying number of images representing different instances of the respective fruits. The images are preprocessed and resized to a uniform size of 224x224 pixels to match the input shape of the model.

## Model Architecture

For this task, a transfer learning approach is employed using the VGG16 model pretrained on the ImageNet dataset. The VGG16 model is a convolutional neural network (CNN) architecture known for its effectiveness in image classification tasks. By leveraging the pre-trained weights of the VGG16 model, we can benefit from the features learned from a large-scale image dataset.

The pretrained VGG16 model is loaded and its top layers are removed to adapt it to the fresh and rotten fruit classification task. A global average pooling layer is added to reduce the spatial dimensions of the output feature maps. This is followed by a dense layer with 6 neurons and a softmax activation function, which enables the model to classify the fruits into their respective categories.

<<<<<<< HEAD
### The Workshop took place 02/11/2022 in our University Lab and was 8 Hours long  
=======
## Training

The model is trained using the Adam optimizer and categorical cross-entropy loss function. To enhance the model's generalization and prevent overfitting, data augmentation techniques are applied to the training dataset. These techniques include rotation, zooming, width and height shifting, and horizontal flipping. By augmenting the data, the model becomes more robust and capable of handling variations in fruit images.

During training, the model is trained for 20 epochs on the augmented training data. The training progress is monitored using the validation dataset, and the model's performance is evaluated based on metrics such as loss and accuracy.

## Fine-tuning (Optional)

After achieving satisfactory validation accuracy, the base model can be unfrozen, and the entire model can be fine-tuned with a low learning rate. Fine-tuning allows the model to further adjust its parameters and learn more specific features from the fresh and rotten fruit images. This step is optional and can potentially improve the model's performance, especially if the dataset is large and diverse.

## Evaluation

To assess the model's performance, it is evaluated multiple times on the validation dataset. The average accuracy is calculated from these evaluations, and if it exceeds 92%, the assessment is considered passed. If the accuracy falls below 92%, further adjustments to the model or training process may be necessary to improve performance.
>>>>>>> 81bfab2 (add: Update README.md)
