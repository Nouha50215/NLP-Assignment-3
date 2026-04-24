Darija N-gram Language Model


A probabilistic n-gram language model trained on Moroccan Darija, supporting both Arabic script and Latin script (Arabizi). Built to run in Google Colab with data loaded directly from Google Drive.


## What it does

It reads your Darija text files from Google Drive, trains an n-gram language model on them, evaluates it using perplexity, and generates new Darija sentences.


## How to use it

Upload the notebook file to Google Colab, then run the cells from top to bottom.

The first cell will ask you to sign in and mount your Google Drive. After that, set the path to your data folder in the second cell. Everything else runs automatically.


## Settings you can change

You can choose the n-gram order, meaning how many words the model looks back at when predicting the next word. A value of 3 is a good default.

You can also choose the smoothing method. Kneser-Ney is recommended for larger datasets. Laplace is simpler and works fine for smaller ones.

If your data files store text under a different field name in JSON format, you can update that in the settings cell as well.


## Data

Put your data folder inside Google Drive. The notebook expects files in plain text, CSV, JSON, or JSONL format. Subfolders are supported and will be read automatically.


## Output

After training, the notebook prints the perplexity scores, the most frequent words and n-grams found in the data, and a few generated sentences. The trained model is saved back to your Google Drive as a JSON file so you can reload it later without retraining.


## Requirements

No installation needed. Google Colab comes with everything required.
