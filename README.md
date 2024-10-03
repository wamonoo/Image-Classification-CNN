# Image-Classification-CNN
We use Kera's flexible graph functional model to build a basic Convolutional Neural Network that can differentiate between cats and dogs. The model is trained on 8000 images and tested on 2000 images of cats and dogs.
The forward propagation for the model is in the form of 
 - CONV2D -> RELU -> MAXPOOL -> CONV2D -> RELU -> MAXPOOL -> FLATTEN -> DENSE

We achieve an accuracy of 80% for predictions on the test data set. 
The model does quite well with relatively high probabilities when predicting new random images of cats or dogs. However, the prediction probabilities reduce as the images get obscured or new additional items are introduced into the images. e.g. The model predicts a dog with 99.9% certainty given a random image of a dog with clear features, but the prediction probability drops when the dog is partially obscured by objects such as furniture or toys. Similarly, for cat images, the model shows high confidence (around 98%) when the image is unambiguous, but this confidence declines significantly as additional elements like shadows or other animals are introduced. 

![image](https://github.com/user-attachments/assets/be628885-df7d-4c73-b53a-a66eb20471e3)


This suggests that while the model is proficient at identifying distinct, high-quality images, its performance weakens when the visual context becomes more complex or when important features are hidden, pointing to a potential need for further training on more diverse or noisy datasets to improve robustness.
The model gets confused when attempting to predict anything that is outside of the training set (cats and dogs). It predicts two images of wolves as a cat and a dog, which is to be expected since the model never had the opportunity to learn wolf images.
