# DNA-Sequence-Classifier-using-NLP

### Goal: In this project,the aim is to apply Machine Learning Classification algorithms on chimpanzee, human and dog gene sequences dataset that can predict genes function based on DNA sequence (coding sequence) alone.

### About the Data set:
Three datasets were used for three different projects, one for human,one for dog and the other for chimpanzee. All the datasets have two features namely sequence and class. The datsets are in text format and present in this repository. 

### About the project: 
After loading the data set the initial step was to perform K-mer counting and converting the sequences into specific length of six and converting into lower case. All the kmers were joined to form a paragraph and Bag of Words were applied to convert words into vectors. Finally, Multinomial Naive Bayes algorithm was applied on the training data and predicted on the test data. Model was evaluated using accuracy score, classification report and confusion matrix.

### Treating DNA sequence as a "language", otherwise known as k-mer counting
A challenge that remains is that none of these above methods results in vectors of uniform length, and that is a requirement for feeding data to a classification or regression algorithm. So with the above methods you have to resort to things like truncating sequences or padding with "n" or "0" to get vectors of uniform length.

DNA and protein sequences can be viewed metaphorically as the language of life. The language encodes instructions as well as function for the molecules that are found in all life forms. The sequence language analogy continues with the genome as the book, subsequences (genes and gene families) are sentences and chapters, k-mers and peptides (motifs) are words, and nucleotide bases and amino acids are the alphabet. Since the analogy seems so apt, it stands to reason that the amazing work done in the natural language processing field should also apply to the natural language of DNA and protein sequences.

The method I use here is simple and easy. I first take the long biological sequence and break it down into k-mer length overlapping “words”. For example, if I use "words" of length 6 (hexamers), “ATGCATGCA” becomes: ‘ATGCAT’, ‘TGCATG’, ‘GCATGC’, ‘CATGCA’. Hence our example sequence is broken down into 4 hexamer words.

Here I am using hexamer “words” but that is arbitrary and word length can be tuned to suit the particular situation. The word length and amount of overlap need to be determined empirically for any given application.

In genomics, we refer to these types of manipulations as "k-mer counting", or counting the occurances of each possible k-mer sequence. There are specialized tools for this, but the Python natural language processing tools make it super easy.
