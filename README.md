# Sentence AutoComplete Tool with Word2Vec and LSTM

This repository contains code for implementing a Sentence AutoComplete Tool using a pre-trained Word2Vec model and LSTM. The tool predicts the next word in a sentence based on the input provided by the user.

## Problem Description

The task is to develop a Sentence AutoComplete Tool that can predict the next word in a sentence. The tool utilizes a pre-trained Word2Vec model, which is used as an embedding layer, and an LSTM model for sequence prediction. The user enters a sentence word by word, and with each input, the tool predicts the next word based on the trained models.

## Dataset

The Enron Sent Corpus Dataset is used for this project. The dataset contains a collection of sentences from the Enron email corpus. The data is tokenized and preprocessed to prepare it for training the models.

## Preparing Data

The dataset is split into samples, where each sample consists of one paragraph. Each paragraph is further split into fixed time steps to create input-output pairs for training the models. The data is divided into training and validation sets as follows:
- Training data: enronsent00 to enronsent10
- Validation data: enronsent11 to enronsent15

## Word2Vec Model

A pre-trained Word2Vec model is used as an embedding layer in the LSTM model. You can choose any pre-trained Word2Vec model of your choice, as long as it is compatible with the Word2Vec format. Optionally, you can also train your own Word2Vec embedding from scratch using techniques explained in the lab.

## Training

The training process involves training the LSTM model using the pre-trained Word2Vec model as the embedding layer. The model is trained on the training data, and the output is the predicted next word in the sentence. The model is evaluated using the validation data.

## Testing

The Sentence AutoComplete Tool allows the user to enter a sentence word by word. With each word entered, the tool predicts the next word using the trained models. The user is prompted to confirm if the predicted word is correct. If it is correct, the tool predicts the word after it. If not, the user can enter the correct word. The loop continues until the user terminates it. The tool can be run multiple times for different input sentences.
