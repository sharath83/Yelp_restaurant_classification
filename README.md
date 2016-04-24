# Yelp_restaurant_classification
Classifying restaurants using user submitted images

Yelp_image_classification.ipynb program extracts features from user submitted images on restaurants from VGG net pretrained model
Paper: Very Deep Convolutional Networks for Large-Scale Image Recognition K. Simonyan, A. Zisserman
arXiv:1409.1556

#VGG16 model - ILSVRC - 2014 competition
#Mean = [103.909, 116.779, 123.68]
#BGR format

I have tried to extract hidden layer activations from different layers of the network for every image and 
averaged the activations of all images belong to one restaurant. I have used the averaged activation values as features for restaurants.

I have used Theano and Keras for extracting layer level weights and activations for images

Multilabel_clf.ipynb code classifies restaurants in to any one of the 9 labels (0-8). I have used svm and random forest classifiers.
Labels:
0: good_for_lunch
1: good_for_dinner
2: takes_reservations
3: outdoor_seating
4: restaurant_is_expensive
5: has_alcohol
6: has_table_service
7: ambience_is_classy
8: good_for_kids

in Multilabel_clf.ipynb, I have setup a cv and thorugh tuning of hyper parameters

You can read about the problem more at: https://www.kaggle.com/c/yelp-restaurant-photo-classification
