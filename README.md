# Darija N-gram Language Model

A probabilistic n-gram language model trained on Moroccan Darija, supporting both Arabic script and Latin script (Arabizi). Built to run in Google Colab with data loaded directly from Google Drive.


## What it does
It reads the Darija text files from Google Drive, trains an n-gram language model on them, evaluates it using perplexity, and generates new Darija sentences.

## Data
The model loaded 500,000 sentences from only 2 Twitter files (tweets.txt and tweets2.txt) before hitting the line limit, totalling around 4.9 million tokens. 

## Vocabulary 
The model learned 510,682 unique word types, which is very large. This is partly because the Twitter data contains URLs, hashtags, mixed languages and noise that inflate the vocabulary artificially.

## Perplexity 
The train perplexity of 20.23 looks good on its own, meaning the model fits what it saw well. However the infinite dev and test perplexity tells us the model frequently assigns zero probability to word combinations it never saw during training. 
This is a classic sign of data sparsity at the trigram level with such a large and noisy vocabulary.

## What the model learned 
Looking at the top n-grams and words, the data quality is the main problem. The most frequent trigram is "https t co" which is a Twitter URL fragment repeated 63,576 times. The top words are dominated by URL parts like "t", "co", "https", French words like "de", "le", "est", "je", and English words like "the", "i". This means the model learned mostly Twitter noise and code-switching rather than clean Darija.

## Generation
The generated sentences reflect exactly this. They mix Arabic, French, English, URLs and random tokens incoherently, which is a direct consequence of the noisy Twitter training data.

## Output
After training, the notebook prints the perplexity scores, the most frequent words and n-grams found in the data, and a few generated sentences. The trained model is saved back to the Google Drive as a JSON file.


