# Melanoma Detection

![CNN](https://d3i71xaburhd42.cloudfront.net/b57ba909756462d812dc20fca157b3972bc1f533/1-Figure1-1.png)

> The task involves constructing a custom convolutional neural network using TensorFlow for the purpose of creating a multiclass classification system. The objective is to develop a CNN model capable of precisely identifying melanoma, a life-threatening form of cancer that becomes increasingly fatal without early detection. Melanoma constitutes 75% of fatalities resulting from skin cancer. Implementing a solution that can assess images and promptly notify dermatologists about the existence of melanoma holds the promise of diminishing the substantial manual labor typically required in the diagnostic process.

> The collection comprises 2357 pictures portraying both malignant and benign oncological conditions, sourced from the International Skin Imaging Collaboration (ISIC). These images were categorized based on the ISIC classification, and all groups contain an equal number of images except for melanomas and moles, where there's a slightly higher representation of images.

The data set contains the following diseases:

- Actinic keratosis
- Basal cell carcinoma
- Dermatofibroma
- Melanoma
- Nevus
- Pigmented benign keratosis
- Seborrheic keratosis
- Squamous cell carcinoma
- Vascular lesion

## Project Pipeline

- __Data Reading/Data Understanding__ → Defining the path for train and test images 
- __Dataset Creation__ → Create train & validation dataset from the train directory with a batch size of 32. Also, make sure you resize your images to 180*180.
- __Dataset visualisation__  → Create a code to visualize one instance of all the nine classes present in the dataset 
- __Model Building & training :__
     - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0,1).
    - Choose an appropriate optimiser and loss function for model training
    - Train the model for ~20 epochs
    - Write your findings after the model fit. You must check if there is any evidence of model overfit or underfit.
- __Chose an appropriate data augmentation strategy to resolve underfitting/overfitting__
- __Model Building & training on the augmented data :__
    - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model rescale images to normalize pixel values between (0,1).
    - Choose an appropriate optimiser and loss function for model training
    - Train the model for ~20 epochs
    - Write your findings after the model fit, see if the earlier issue is resolved or not?
- __Class distribution:__ Examine the current class distribution in the training dataset 
    - Which class has the least number of samples?
    - Which classes dominate the data in terms of the proportionate number of samples?
- __Handling class imbalances:__ Rectify class imbalances present in the training dataset with Augmentor library.
- __Model Building & training on the rectified class imbalance data :__
    - Create a CNN model, which can accurately detect 9 classes present in the dataset. While building the model, rescale images to normalize pixel values between (0,1).
    - Choose an appropriate optimiser and loss function for model training
    - Train the model for ~30 epochs
    - Write your findings after the model fit, see if the issues are resolved or not?

## Conclusions

We observe gradual improvement from Model 1 to Model 3:

- Model 1: Simple CNN Model
     - Accuracy: 0.9244 | Validation accuracy : 0.5391

- Model 2: Augmented data with droupout
     - Accuracy: 0.5965 | Validation accuracy : 0.5369

- Model 3: Class rebalance,BatchNormalization with Dropout
     - Accuracy: 0.9329 | Validation accuracy : 0.7929

With the right hyper-parameter tuning, accuracy can be improved even more. We can experiment with different CNN configurations, loss functions, optimizers, and layer counts to see accuracy pattern.

## Technologies Used
- NumPy - version 1.23.5
- Pandas - version 1.5.3
- keras - version 2.12.0
- Tensorflow version 2.12.0

## Contact
Created by __Abhishek Arora__
