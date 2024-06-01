# Image Caption Generation

Data: https://www.kaggle.com/datasets/adityajn105/flickr8k

1. Load the data and create a dictionary of descriptions
2. clean the descriptions - remove stopwords, punctuation, hanging letters, numbers.
3. Extract features from images using Xception model and store them in a file for further use
4. load the images, featues and cleaned descriptions into variables train_imgs, train_features, train_descriptions respectively.
5. create a vocabulary list from descriptions
6. tokenize the descriptions and store them in a pickle file
7. find the maximum length of descriptions to ensure that all sentences given for training are of same length
