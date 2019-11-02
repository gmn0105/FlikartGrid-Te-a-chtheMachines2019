# FlipkartGrid-TeachtheMachines2019
* This is a single object localization task.
* The expected output is a bounding box localizing the object in a given image.
* We use an autoencoder based deep neural network for this task.
* The autoencoder assigns each pixel with a probabilty score between 0 and 1 using softmax (0 not being a part of the object and 1 being a part of the object to be localized).
* Then using the farthest pixels with probabilty score >= 0.95 representing the corners of a rectangle, we draw the bounding box.
* We train it using binary crossentropy loss averaged over all the pixels of the image.
* The best scores are obtained by tuning various hyperparameters like number of encoder/decoder layers, number hidden units in the layers, batch size, optimizers etc.
* The metric used is Intersection over Union
* The inital part of the code is applicable only when you are using Google Colab.
* The dataset it a property of Flipkart India and cannot be shared publicly.