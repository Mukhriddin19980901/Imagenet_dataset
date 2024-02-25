# Imagenet_dataset
Fully trained model with large Imagenet dataset using ResNet50

**Data Preparation:** I load the ImageNet dataset, specifically the training images, and preprocess them. The dataset is organized into folders, each representing a class, and I load a few images from each class.
    
![](https://github.com/Mukhriddin19980901/Imagenet_dataset/assets/86052339/51cfc702-b488-44c6-9e5a-c38fdf72d3c9)

![](https://github.com/Mukhriddin19980901/Imagenet_dataset/assets/86052339/6cca870f-17d7-46b2-9653-b8048b27c0bf)


**Model Building (Initial Attempt):** I instantiate a ResNet-50 model with pre-trained weights from ImageNet and include the top layers for classification. Then, I make predictions on the loaded dataset and evaluate the model's accuracy.

     102967424/102967424 [==============================] - 1s 0us/step
     
     Model: "resnet50"
     
     Layer (type)                   Output Shape         Param #     Connected to                     
     ==================================================================================================
     input_1 (InputLayer)           [(None, 224, 224, 3  0           []                               )]    

     .....

     predictions (Dense)            (None, 1000)         2049000     ['avg_pool[0][0]']               
                                                                                                  
     ==================================================================================================
     
     _______________________________________________________________________________________
     
**Visualization:** I visualize some of the original images and the corresponding predictions made by the initial ResNet-50 model.

![](https://github.com/Mukhriddin19980901/Imagenet_dataset/assets/86052339/75355402-7256-42fc-acec-1d897c7dd8ff)



**Transfer Learning:** Next, I attempt transfer learning by using the ResNet-50 architecture as a feature extractor. I freeze the pre-trained layers and add new fully connected layers on top for fine-tuning to my specific classification task.

**Model Evaluation (Transfer Learning):** After fine-tuning, I make predictions with the transfer learning model and evaluate its accuracy.

**Visualization of Transfer Learning Results:** I visualize some of the images again, this time showing the predictions made by the transfer learning model.

**Accuracy Comparison:** Finally, I compare the accuracies of both the initial ResNet-50 model and the transfer learning model to see which performs better.

Overall, my project involves exploring the effectiveness of ResNet-50 for image classification on the ImageNet dataset, both with and without transfer learning, and comparing the performance of the models I build. This type of project is common in the field of deep learning, particularly for tasks like image classification.


<img src="https://github.com/Mukhriddin19980901/Imagenet_dataset/blob/main/images/resnet_architect.jpg" height="400" width="700"/>
ResNet-50 is a convolutional neural network (CNN) architecture that is part of the ResNet (Residual Network) family, developed by Microsoft Research. It is known for its deep structure and effectiveness in image recognition tasks, particularly in the context of the ImageNet Large Scale Visual Recognition Challenge (ILSVRC).
ResNet-50 is effective due to its deep architecture, which allows it to capture increasingly complex patterns in the input images. The use of residual blocks enables training of very deep networks without encountering the degradation problem, leading to improved accuracy in image recognition tasks.
