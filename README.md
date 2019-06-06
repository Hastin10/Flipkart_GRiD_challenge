# Flipkart_GRiD_challenge
Our team's submission for the Flipkart GRiD Challenge (https://dare2compete.com/o/Flipkart-GRiD-Teach-The-Machines-2019-74928), a competition where participants had to predict the bounding box co-ordinates for the object given in the image.

This repository contains the code submitted by us in the third round of the competition. The deep learning frameworks used are-TensorFlow and Keras.

In the second round of the competition, our team achieved a rank of 98 out of the 6734 participants on the public leaderboard with an accuracy of 87.17%.(https://dare2compete.com/hackathon/detail/200)

In the third round, we were given the same task of predicting the bounding box co-ordinates as in the second round, but we were provided with more training data. First of all, we needed to convert the images given in sizes of 640x480 to a size of 224x224 since that is the standard size for the input to a ResNet architecture.
We decided to use an ensemble of ResNet-18 and ResNet-50 since we had used ResNet-18 in the second round and achieved an accuracy of 87.17%. The loss function used is smooth L1 loss and the metric for measuring accuracy is IoU(Intersection over Union).

The code for ResNet-50 is in the file 'resnet50.py', for ResNet-18 with a threshold of 0.75, 'resnet18_75.py', and for ResNet-18 with a threshold of 0.80, 'resnet18.py'. The file 'prediction.py' contains the code used for prediction on the test images, we used an ensemble of all the 3 models mentioned above for test images and achieved an accuracy of 90.7%(https://dare2compete.com/hackathon/detail/217).

Code created in collaboration with abhinavraj23 and Smit Shah.
