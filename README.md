# X-ray-Classification
Classify various radiology images into respective categories.Being done using various shape and texture features for feature extraction and SVM for classification.
main_feature_extraction.m calculates the feature vector for a given category of images. A csv file is obtained containing the following feature vector of the images.
It uses the functions 
-> feature_vector.m  which computes the shape histogram and the 
-> density histogram from the function density_histogram.m 
-> on various subblocks in an image which is computed from the function subblocks.m
Every image is made of size 512x512 before extracting the features and in case of any dimension being less than 512, it is padded with zeros to make it 512x512 using padding.m. (No images have dimensions greater than 512).
main_classification.m is used to do the classification on the obtained training and testing feature vectors using a 
-> one vs all svm obtained through the function multisvm.m which gives the accuracy_train as well as accuracy_test.
