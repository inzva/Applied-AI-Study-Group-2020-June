# Applied-AI-Study-Group

This is the repository for the content of inzva 2020-June Applied AI Study Group, guided by Ahmet Melek and Onur Boyar.

You can see all 4 weeks from our playlist on YouTube: https://www.youtube.com/playlist?list=PLhnxo6HZwBgnTokZUfwM-sM0-DXRyp-rl

In the group we have worked on these subjects:

* Frameworks: Tensorflow, Keras Functional API, Keras Sequential API, Pytorch

* Topics: Image Classification, Image Localisation, Image Segmentation, NLP, Anomaly Detection, Recommender Systems

* Architectures - Methods: Artificial Neural Networks (Fully-Connected Neural Networks), Convolutional Neural Networks (CNN), Recurrent Neural Networks (RNN, LSTM, GRU), Autoencoders, Denoising Autoencoders, Isolating Forest, Local Outlier Factor, XGBoost, FunkSVD.

* Environments: Google Colab, Jupyter Notebook (Local)

## Weekly Summaries

### Week1 - Computer Vision

We have worked on six problems:

* Image Classification with MNIST dataset on tensorflow, using Fully-Connected Neural Networks.

* Image Classification with MNIST dataset on keras functional API, using Convolutional Neural Networks.

* Image Classification with CIFAR-10 dataset on keras sequential API, using Convolutional Neural Networks.

* Image Localisation with Kaggle Facial Keypoint Detection dataset on keras sequential API, using Convolutional Neural Networks.

* Image Localisation with Kaggle Facial Keypoint Detection dataset on Pytorch, using Convolutional Neural Networks.

* Image Segmentation with testing on random images from internet on Pytorch, using pretrained resnet101 model.

For all examples in Week1, we have worked on Google Colab.

### Homework 1

In homework one, participants take an aligned hand image dataset with keypoint labels, and try to preprocess the dataset and make regression on the keypoint coordinates.


### Week2 - Natural Language Processing
We have worked on four problems.

* Motivating example for word embeddings with Keras

* Recommender system using word embeddings and wikipedia data with Keras

* Spam text classification example with SimpleRNN, GRU and LSTM layers on Keras

* Machine Translation example with different Recurrent Neural Networks structures and different layer types. We create English to French translation model using Keras.


### Homework 2
In homework two, participants are asked to create a book recommendation system using Online Retail data. Sequences of bought items can be used to feed the word2vec model to create such system.


### Week 3 - Various Topics

We have worked on four problems:

* Hand Joint Coordinate Detection (solution of homework1) with CNNs, on Rovit Hand Pose Estimation Dataset.

* Anomaly Detection with LSTM Autoencoders, on Bearing Data Center dataset.

* Oil Price Prediction with LSTM, on oil price index.

* Occlusion Restoration with Conditional ImageGANs, on our custom dataset that is built upon UTK Faces.

We both used locally hosted Jupyter Notebooks and Google Colab.

### Homework 3

In homework three, participants practice on data acquisition (scraping) with a tool specialized on scraping news sites. They try to make use of an deep learning natural language processing library to obtain a premade language model. They also optionally develop their own models for language modelling.


### Week4 - Anoamly Detection & Recommender Systems

In last week of Applied AI program we have worked on Anomaly Detection and Recommender System problems. For anomaly detection, we use KDDCUP'99 dataset and we try to classify Normal and Probing labels. For recommender system models, we use MovieLens dataset to create different recommender system models.

There are three different notebooks in this week.

* Anomaly Detection Notebook: Includes Isolation Forest, Local Outlier Factor, Autoencoder and XGBoost models for Anomaly Detection.

* Recompy, Matrix Factorization Based Recommender System : FunkSVD algorithm is applied to create Recommender System model.

* Mult-DAE: Multinomial Denoising Autoencoder model is implemented to create a recommender system algorithm which works with implicit feedback.
