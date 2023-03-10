# Bloc_4
**Deep learning project for certification**

This project aims at building a spam detector for the AT&T company, that can automatically flag spams as they come based sollely on the sms' content.  

> Video link of the project : 👉 https://share.vidyard.com/watch/4gwd2x1uxZKdybAWHqCAKa? 👈

Contact : Lise Gnos  
email : lise.gnos@gmail.com  

## 1/ Building a deep learning model from scratch

> Notebook : 'deep_learning/project_spam_detector.ipynb'  

This notebook is used to build a simple deep learning model.  

In this notebook, the following steps are performed :  
- load the dataset
- perform EDA
- do preprocessing : clean the text (lower case, lemmatization, removing STOP words...) and tokenize the text
- build simpleRNN, GRU and LSTM models
- compare the results.

Please note that the lines of code for saving files were commented.

## 2/ Transfer learning

> Notebook : 'deep_learning/project_spam_detector_TL.ipynb'  

This notebook is used to train an already pre-trained model : small BERT for word embedding.

In this notebook, the following steps are performed :  
- load the dataset that was already cleaned in the 'deep_learning/project_spam_detector.ipynb' notebook. The clean dataset can be found at 'deep_learning/src/spam_clean.csv'.
- build the small BERT model with the matching preprocess model
- compare the results with the GRU model.

The following links helped me to build the small BERT model :  
https://blog.tensorflow.org/2020/12/making-bert-easier-with-preprocessing-models-from-tensorflow-hub.html  
https://tfhub.dev/google/collections/bert/1  
https://www.tensorflow.org/text/tutorials/classify_text_with_bert?hl=en  
https://tfhub.dev/tensorflow/small_bert/bert_en_uncased_L-2_H-128_A-2/2  


👉 For each model that was trained, checkpoints were saved in order to be able to load the model at a given epoch. All the files can be found in the folders 'deep_learning/trainingRNN', 'deep_learning/trainingGRU', 'deep_learning/trainingLSTM', 'deep_learning/trainingTL'.  

👉 All the saved models and their history can be found in the folder 'deep_learning/content'.

