MaskedPOSAugmentedData.csv
This file contains word embeddings of 6659 tokens augmented with POS tagging and word importance score. The embedding size for each token is a one dimensional vector of length 768 by 1. Due to augmenting POS tagging, the new feature vector becomes a size of 769 by 1. So now the total feature matrix size is 6659 by 769. In the dataset the final column represents the word importance score. 



MaskedSentenceWithImportanceTag.csv
This dataset contains the newly generated sentence using standard Masking technique and their corresponding token-wise importance score.


Data cleaning procedure
Using several steps, we have cleaned the “switchboard corpus” that we are using for this particular study. Here are the steps we followed:
– Convert all the letter into lower case
– Punctuation has be removed
– Numbers or Cardinal values have been converted to text representation 
– We use lemmatization techniques to eradicate the possibility of multiple versions of the same word token.




Annotation Instruction
If researchers intend to produce additional masked text for further the size of the dataset, we recommend using the method we described in the paper.
However, if someone wants to manually annotate the words or tokens in a dataset, it is important to remember that annotators need to put a score on each word based on its relative importance within a sentence or the information available around that text. It may not be appropriate to allow annotators to read the whole document first and then conduct annotation. Also using multiple annotators is recommended otherwise interrater agreement may not work well.

Test and training data splitting
As described in the paper, during our experiment, we have retained 10% of data as test data and use 90% data to train the models. For proper replication, we recommend reading our paper thoroughly. 

We understand that the dataset size is relatively small for training and testing a model that might be reliable. It is important to remember that data annotation with this particular user group might be challenging. 

N.B: While augmenting the new feature within the dataset, a portion of data has been excluded during the data curation phase. For validation, we have replicated the previous models so that we can measure how the dataset can perform with this newly formed dataset. 
