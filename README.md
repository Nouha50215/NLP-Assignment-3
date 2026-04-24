# Darija N-gram Language Model


A probabilistic n-gram language model trained on Moroccan Darija, supporting both Arabic script and Latin script (Arabizi). Built to run in Google Colab with data loaded directly from Google Drive.


## What it does

It reads your Darija text files from Google Drive, trains an n-gram language model on them, evaluates it using perplexity, and generates new Darija sentences.


## How to use it

Upload the notebook file to Google Colab, then run the cells from top to bottom.


## Settings you can change

We can choose the n-gram order, meaning how many words the model looks back at when predicting the next word. we choose 3 as default.

Smoothing method


## Output

After training, the notebook prints the perplexity scores, the most frequent words and n-grams found in the data, and a few generated sentences. The trained model is saved back to your Google Drive as a JSON file so you can reload it later without retraining.


