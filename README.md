
Part 1: Image Classification with MNIST

Setup and Data Preprocessing:

Loads the MNIST dataset of handwritten digits.

Normalizes and reshapes images to a size compatible with the models (28x28 pixels).

Model A (Custom CNN):

Builds a simple convolutional neural network (CNN) for digit classification.

Trains for 10 epochs, reaching high accuracy (99.22%) on the test data.

Model A is efficient, with low training time and high accuracy for this dataset.

Model B (VGG16 Transfer Learning):

Converts grayscale images to RGB, resizes them to 32x32, and uses a pre-trained VGG16 model.

Freezes the pre-trained layers and adds new layers for classification.

Trains for 10 epochs, achieving 97.33% accuracy on the test data.

Model B takes longer to train and performs slightly worse than Model A on this simpler dataset.

Comparison:

Model A: Higher accuracy, lower loss, faster training.

Model B: Showcases transfer learning but performs less effectively for MNIST.

Part 2: Sentiment Analysis with Text Data

Data Loading and Processing:

Loads an airline tweets dataset and an IMDB movie review dataset.

Prepares text data by tokenizing, padding, and converting sentiment labels (positive = 1, negative = 0).

Model C (Trained on Airline Tweets):

Builds an LSTM model for sentiment analysis.

Trains on airline tweets data, reaching 90.88% accuracy.

Performs well, likely due to training on relevant data.

Model D (Trained on IMDB Reviews):

The same model structure as Model C, but trained on IMDB reviews.

Evaluated on the airline tweets dataset, achieving only 47.37% accuracy.

Shows poor generalization due to differences in dataset context and language.

Conclusion:

Model C (trained on airline tweets) performs significantly better on airline tweets.

Model D (trained on IMDB reviews) struggles with airline tweets, highlighting the importance of matching training data with target application data.

This code demonstrates:

How dataset relevance impacts model performance.

How a model trained from scratch can outperform transfer learning on simple tasks.

The challenges of transfer learning when datasets differ significantly in context.
