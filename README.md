# brain-tumor-det-and-segmentation
Detection of brain tumour using pretrained VGG-16 and segmentation using U-net

This was a group project for DA-202 Applied Machine learning course.

Dataset used is LGG segmentation dataset available on kaggle.(link in report)

Initially we did data preprocessing to merge the MRI images and the mask images along with the labels in the dataframe and then data augmentation techniques were used as the dataset was limited to train the model. Details given in the report. Literature about the techniques is easily available on the net so you can refer from there if you are interested.

For the classification task VGG-16 was used, pretrained on imagenet. Convolutional layers were pretrained but the dense layers were built and trained by us. Adam was used as optimiser and the cost function used is binary cross entropy along with sigmoid as the activation function. We also added regularisation in the form of drop out layers to avoid overfitting.

For the segmentation task U-net architecture was used which is one of the best architectures in the field of medical segmentation. For architecture details refer the report.  Dice coefficient was used as the metric and the loss used is negative of dice coefficient.

In the detection task we got an accuracy of 89% and for the segmentation task we got the dice coeffiecient value of 0.81 on the test data.

