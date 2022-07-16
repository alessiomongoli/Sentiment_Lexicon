# PROJECT of Deep Natural language proccessin

In this project we try to replicate and to expand  the paper 'Domain-Specific Sentiment Lexicons Induced from Labeled Documents' (https://aclanthology.org/2020.coling-main.578/).

## File Generale
If you want to run our first experiment explained in the paper, you should open File Generale's link colab and set the parameter of the cell 8:
- CATEGORY: specify the starter dataset_review.There are three choose: #"reviews_Apps_for_Android" #reviews_Apps_for_Android or reviews_Grocery_and_Gourmet_Food


- SAVE_DATAFRAME: if you want to save dataframe with [Word, Polarity, Frequencies]

- CHECKPOINT_PATH


- NEGATION_TYPE: the type of detect negation. normal: we add the prefix "neg", to the word preceded by not ex."I don't have a car" -> "I neg_have a car"
                                            all_words: we add the prefix "neg", to all word after not   ex. "I don't have a car" ->"I neg_have neg_a neg_car"
                                            no_negation



- NEGATION_MEAN: When Negation_MEAN is true we consider also the Neg_word to adjust polarity of the word without Neg:
                  New Polarity [word]=(Polarity[word]+ Polarity[NEG_word])/2


This script run predictions on the Imdb and Twitter dataset and return the accuracy.




## EXPERIMENT PRICE

Ify ou want to run our experiment regarding the evolution of polarity with the changing of the price, you should open the Experiment Price's link colab and set the parameter of the cell 11:

-CATEGORY: specify the dataset review dataset on which you want perform the analysis. Wehave used the reviews_Musical_Instruments dataset


-PATH_CATEGORY the path where we download the dataset


-PATH_METADATA the path where we downoald the metadat


-negation_type  the type of detect negation. normal: we add the prefix "neg", to the word preceded by not ex."I don't have a car" -> "I neg_have a car"
                                            all_words: we add the prefix "neg", to all word after not   ex. "I don't have a car" ->"I neg_have neg_a neg_car"
                                            no_negation. We have perfomed with "normal" negation.
