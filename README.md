# Exploring Philosophical Texts Across Gender & Time with Text Analytics

## Project Overview
Text Analytics is a powerful tool to help reveal and extract cultural patterns from large quantities of texts. The goal of this project is to use text analytics to explore cultural patterns in philosophical texts. Main topics and cultural themes are analyzed among the texts as a whole, as well as through time and across genders.
 
#### Key Questions:
- What are the most important topics philosophers are concerned with?
- Do male and female philosophers explore different or similar topics?
- Do topics change or vary across different eras?

## Project Data
For this project, 20 philosophical texts were collected. Thirteen texts are by male philosophers, and span from the 400th century B.C. to the 21st century A.D. Ten of these philosophical texts were written in the Western world, and three by men in South America and Asia. Seven texts are written by female Western philosophers, spanning from the 19th century through 21st century AD. These texts were collected from Project Gutenberg, and other online document archives. The texts were obtained in Plain-Text format, for easier use in data cleaning, parsing, and manipulation. Due to the necessity of the Plain-Text format, the available texts were limited, especially for the female philosophers. Most (known) published female philosophers are from the modern era, with limited free access to their works in the necessary format.

Due to these limitations, the distribution of philosophical texts is not even across era and gender. The imbalance likely affects the results, and is taken into account when analyzing the texts. Further exploration with more texts would provide greater understanding into the cultural themes present in philosophical literature, and should be considered for future studies. However, the twenty texts collected for this project still provides a basic understanding of cultural patterns, and addresses the key questions this project aims to explore.

## Methodology
The first project notebook, [‘CleanTexts_BuildTables.ipynb’](https://github.com/HaleyEgan/Text-Analytics-Philosophy-Project/blob/main/CleanTexts_BuildTables.ipynb), imports and cleans the 20 philosophical texts, and then builds the dataframes LIB, DOC, TOKEN, and VOCAB. LIB contains basic metadata about each text, DOC contains preserved paragraphs of each text and the appropriate OHCO index, TOKEN contains an OHCO index and parts-of-speech tags derived from NLTK, and VOCAB contains NLTK to extract stopwords, porter stems, and 'pos_max' that contains the most frequent parts-of-speech tags from the TOKEN table. These are saved as csv files to use for text exploration and analysis in the other project notebooks.

The second notebook, ‘TFIDF_comparingAuhtors.ipynb’, builds a TF-IDF matrix, creates Bag-of-Words, and performs PCA to see if Harriet Taylor Mill wrote Utilitarianism, a text attributed to her husband, John Stuart Mill.

The third project notebook, ‘TopicModeling.ipynb’, contains code for LDA and Topic Modeling. The notebook contains an exploration of the overall topics in the texts, as well as the topics in texts grouped by gender and texts grouped by time period.

The fourth notebook, ‘WordEmbeddings.ipynb’, uses word2vec, t-SNE plots, and semantic algebra to explore word use, word similarities and differences, and word evolution between texts, genders, and over time.

The fifth project notebook, ‘SentimentAnalysis.ipynb’, used the NCR lexicon to explore and analyze the top emotions per text, per gender grouping, and per time period. Plots are used to visualize the results.
 
