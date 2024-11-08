# Multi-Task Image Classification with Transfer Learning

## Abstract

In this project, we explored the use of transfer learning to classify images of monuments from around the world using the EfficientNetB0 and VGG16 architectures. Our primary goal was to develop efficient and accurate models forlandmark and category classification. We formulated several hypotheses and experimented with different approaches, including data augmentation and normalization techniques, freezing and unfreezing layers, adjusting learning rates, and incorporating dropout layers. We achieved an F1-Score of 1.00 and 0.97 for categories and landmarks classification, respectively, using the EfficientNetB0 model with a Sequential learning approach. Future work includes exploring different architectures and regularization techniques and investigating the underperformance of some approaches. Overall, our results demonstrate the effectiveness of transfer learning and its potential for improving the accuracy and efficiency of deep learning models.

## Approaches :

### 1. Parallel Learning (Multi-output model) :
Compiling the model just once with 2 different output layers for each classification task.

### 2. Sequential Learning :
Compiling and training the model for Categories Task first and then doing the same for Landmarks Task using the same model (same weights) and swapping out the output layer.

### 3. Sequential Learning :
Compiling and training the model for Landmarks Task first and then doing the same for Landmarks Task using the same model (same weights) and swapping out the output layer.

### 4. Sequential Learning :
Compiling and training the model for Categories Task first and using the output of the first model as an additional feature for the Landmarks Task.

### 5. Sequential Learning :
Compiling and training the model for Landmarks Task first and using the output of the first model as an additional feature for the Categories Task.

## Model Selection

It was established that training for landmarks task first was better because there were fewer images per class in the training set. It was better for the model to emphasize more on the landmarks task. Since there were a lot of images per class for the categories task and on top of that, there were fewer numbers of classes, this was an easier task (in terms of predictions) compared to the landmarks task. So upon research, these inferences were made that it is much better to train for the landmarks dataset first, and then we could use the same model with the same weights for the categories task.

![image](https://github.com/user-attachments/assets/6208b838-6817-44e3-b3a9-50bcb109bcf4)


## Results

We implemented transfer learning for multiclass classification of categories and landmarks using the EfficientNetB0 pre-trained model. We experimented with multiple approaches and achieved the best F1-Score of 1.00 and 0.97 respectively on test sets using the Sequential approach of first training the model for Landmarks task and then using the same model (only swapping out the output layer) for the Categories task.

### Model Performance for Landmarks Task
![image](https://github.com/user-attachments/assets/04ab8dd7-7a46-4274-aa3c-d5a7f3d0c4e1)


### Model Performance for Categories Task
![image](https://github.com/user-attachments/assets/54357674-c5f8-43b6-a493-7081b1f6e530)

## Conclusions

This project utilized transfer learning with EfficientNetB0 and VGG16 architectures to classify images of Monuments around the World. The EfficientNetB0 model was found to be more suitable, achieving F1-Scores of 1.00 and 0.97 for Categories and Landmarks Classification respectively. Future work includes exploring other architectures, regularization techniques, and unsupervised learning methods to improve performance and data quality. Overall, this project highlights the potential of transfer learning in image classification tasks.

