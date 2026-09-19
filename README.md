# Skin-Cancer-Classification-Convolutional-Neural-Network
<img width="1920" height="1281" alt="image" src="[https://github.com/user-attachments/assets/644bc6f9-5464-466c-bbec-fa237293d07a](https://www.google.com/url?sa=t&source=web&rct=j&url=https%3A%2F%2Ficons8.com%2Ficon%2Fc30f3wff0kBK%2Fskin-cancer&ved=0CBYQjRxqFwoTCPCE6Yqh-5YDFQAAAAAdAAAAABA3&opi=89978449)" />

## Overview
This repository contains a machine learning project focused on skin cancer classification. The data being analyzed is from the **HAM10000 dataset** and consists of dermatoscopic images representing seven different types of skin lesions. The primary objective is to build a convolutional neural network (CNN) model that accurately classifies skin lesions into their respective diagnostic categories. By supporting automated and more consistent lesion classification, this model may contribute to earlier detection and assist in the diagnosis of skin cancer. 

## Problem 
In this project, we analyze a dataset containing dermatoscopic images of skin lesions representing seven different diagnostic categories. This dataset is highly imbalanced, with the _nv_ (melanocytic nevi) category containing substantially more samples than several of the other lesion types. Our goal is to develop a CNN capable of accurately classifying skin lesions into their respective diagnostic categories because several of the lesion types have visually similar characteristics, resulting in accurately distinguishing between classes being a challenging classification problem. 

## Objectives
The objectives of the project are as follows:
1. **Dataset Exploration and Class Balancing**: Explore the HAM10000 dataset and address the imbalance between the seven skin lesion categories.
- Examine the distribution of lesion diagnoses
- Explore patient sex, age, and lesion localization
- Separate the dataset into the seven diagnosis classes
- Resample each class to approximately 500 images
2. **Image Loading and Preprocessing:** Prepare the skin lesion images for use in the CNN.
- Locate the corresponding image files using the image IDs
- Resize the images to 64 x 64 pixels
- Convert the images into NumPy arrays
- Normalize pixel values to a range of 0-1
- Convert the diagnosis labels into categorical values
- Split the dataset into training and testing sets
3. **CNN Model Development and Training:** Build and train a CNN to classify the seven types of skin lesions.
- Implement convolutional layers to extract visual features
- Apply max pooling to reduce image dimensions
- Use dropout to help reduce overfitting
- Flatten extracted features before classification
- Use a dense output layer with seven classes
- Train the model using the Adam optimizer and categorical cross-entropy loss
4. **Model Evaluation and Analysis:** Evaluate the CNN's ability to classify unseen skin lesion images.
- Examine the training and validation accuracy and loss
- Calculate the model's overall test accuracy
- Generate predictions for the test images
- Construct a confusion matrix to compare actual and predicted diagnoses
- Analyze misclassification between the seven lesion categories

## Results & Discussion
The CNN successfully learned meaningful visual features from the skin lesion images, as evidenced by the training accuracy increasing from approximately 16% during the first epoch to approximately 80% by the final epoch. Additionally, the validation accuracy increased from around 15% to 74%. The final reported test accuracy was approximately 73.6%, which indicates that the model could accurately classify roughly three out of every four test images.

The confusion matrix showed that the majority of predictions were correctly classified along the diagonal. However, several lesion categories had notable misclassification, suggesting that some lesion types have similar visual characteristics that make them more difficult to distinguish in the CNN. The training and validation curves also showed a moderate gap between training and validation accuracy, suggesting some degree of overfitting.

## Next Steps
Several improvements could be explored in future iterations of the project:
- **Apply image augmentation:** Introduce transformations such as horizontal flipping, rotation, and zooming to expose the CNN to greater image variability and potentially improve generalization.
- **Improve the CNN architecture:** Gradually increase the number of convolutional filters and incorporate Batch Normalization to improve feature learning and training stability.
- **Use training callbacks:** Apply early stopping, learning-rate reduction, and model checkpointing based on validation performance to help prevent overfitting and retain the best-performing model.

## File Descriptions
- Skin Cancer Classification.ipynb : Google Colab code with all information from the aforementioned Objectives as well as key observations and additional information in the comments.
- README.md : This file, providing the overview of the project.
