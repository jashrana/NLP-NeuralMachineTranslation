# NLP NeuralMachineTranslation
Training on a Neural Machine Translation (NMT) system for English-Irish translation where English is the source language and Irish is the target language.

Code Files:
1. 22222806_RANA.ipynb


# University of Galway
# Assignment (Neural Machine Translation)

This Assignment focuses on the training on a Neural Machine Translation (NMT) system for English-Irish translation where English is the source language and Irish is the target language. 

## Task 1 - Data Collection and Preprocessing (10 points)

## Task 1a. Data Loading (5 pts)
Dataset: https://www.dropbox.com/s/zkgclwc9hrx7y93/DGT-en-ga.txt.zip?dl=0 
*  Download a English-Irish dataset and decompress it. The `DGT.en-ga.en` file contains a list english sentences and `DGT.en-ga.ga` contains the paralell Irish sentences. Read both files into the Jupyter environment and load them into a pandas dataframe. 
* Randomly sample 12,000 rows.
* Split the sampled data into train (10k), development (1k) and test set (1k)

## Task 1b. Preprocessing (5 pts)
* Add '<bof\>' to denote beginning of sentence and '<eos\>' to denote the end of the sentence to each target line.
* Perform the following pre-processing steps:
  * Lowercase the text
  * Remove all punctuation
  * tokenize the text 
*  Build seperate vocabularies for each language. 
* Assign each unique word an id value 
* Print statistics on the selected dataset:
  * Number of samples
  * Number of unique source language tokens
  * Number of unique target language tokens
  * Max sequence length of source language
  * Max sequence length of target language


## Task 2. Model Implementation and Training (30 pts)

## Task 2a. Encoder-Decoder Model Implementation (10 pts)
Implement an Encoder-Decoder model in Pytorch with the following components
* A single layer RNN based encoder. 
* A single layer RNN based decoder
* A Encoder-Decoder model based on the above components that support sequence-to-sequence modelling. For the encoder/decoder you can use RNN, LSTMs or GRU. Use a hidden dimension of 256 or less depending on your compute constraints. 

## Task 2b. Training (10 pts)
Implement the code to train the Encoder-Decoder model on the Irish-English data. You will write code for the following:
* Training, validation and test dataloaders 
* A training loop which trains the model for 5 epoch. Evaluate the loop at the end of each Epoch. Print out the train perplexity and validation perplexity after each epoch.

## Task 3. Improving NMT using Attention (10 pts) 
Extend the Encoder-Decoder model from Task 2 with the attention mechanism. Retrain the model and evaluate on test set. Print the updated average BLEU score on the test set. In a few sentences explains which model is the best for translation. 