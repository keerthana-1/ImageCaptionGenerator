# Image Caption Generation

Data: https://www.kaggle.com/datasets/adityajn105/flickr8k

1. Load the data and create a dictionary of descriptions
2. clean the descriptions - remove stopwords, punctuation, hanging letters, numbers.
3. Extract features from images using Xception model and store them in a file for further use
4. load the images, featues and cleaned descriptions into variables train_imgs, train_features, train_descriptions respectively.
5. create a vocabulary list from descriptions
6. tokenize the descriptions and store them in a pickle file
7. find the maximum length of descriptions to ensure that all sentences given for training are of same length
8. For each descriprion, tokenize it and split the sequence into input (in_seq) and output (out_seq) pairs. The input is the sequence up to but not including the current word, and the output is the current word.
9. Pad the input sequence to ensure it has a length of max_length.
10. One-hot encode the output sequence (the next word). vocab_size is the total number of unique words in the vocabulary.
11. Append the image feature, input sequence, and output sequence to their respective lists.
12. Convert the lists to numpy arrays and return them.
13. compile a neural network model for image captioning, which combines features extracted from images using a Convolutional Neural Network (CNN) with sequences of words processed by an LSTM network. The model aims to predict the next word in a sequence given an image and a partial sequence of words (caption)
14. processes the image features through a dense network and the text sequences through an embedding layer and LSTM. The outputs of these two paths are merged, further processed through dense layers, and finally, a softmax layer predicts the next word in the sequence.
15. The model is compiled with categorical cross-entropy loss and the Adam optimizer.


