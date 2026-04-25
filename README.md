# Darija N-gram Language Model


A probabilistic n-gram language model trained on Moroccan Darija, supporting both Arabic script and Latin script (Arabizi). Built to run in Google Colab with data loaded directly from Google Drive.


## What it does

It reads the Darija text files from Google Drive, trains an n-gram language model on them, evaluates it using perplexity, and generates new Darija sentences.


## Data

Loads the files from Google Colab and stops as soon as it hits 500,000 lines total, then run the cells from top to bottom.


## Output

After training, the notebook prints the perplexity scores, the most frequent words and n-grams found in the data, and a few generated sentences. The trained model is saved back to your Google Drive as a JSON file so you can reload it later without retraining.


