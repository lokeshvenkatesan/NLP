NLP: Tokenization , Stemming , Lemmatization , Bag of Words ,TF-IDF , POS

Natural language processing (NLP) is a branch of Artificial intelligence (AI) that helps computers understand, interpret and manipulate and respond to human in their natural language.

Tokenization
Tokenization is the process breaking complex data like paragraphs into simple units called tokens.
Sentence tokenization : split a paragraph into list of sentences using sent_tokenize() method
Word tokenization : split a sentence into list of words using word_tokenize() method

Import all the libraries required to perform tokenization on input data.
    from nltk.tokenize import sent_tokenize, word_tokenizefrom
    

Some other important terms related to word Tokenization are:
Bigrams: Tokens consist of two consecutive words known as bigrams.
Trigrams: Tokens consist of three consecutive words known as trigrams.
Ngrams: Tokens consist of ’N’ number of consecutive words known as ngrams
Data Cleaning plays important role in NLP to remove noise from data.
Stopwords : refers to the most common words in a language (such as “the”, “a”, “an”, “in”) which helps in formation of sentence to make sense, but these words does not provide any significance in language processing so remove it .

Stemming
Stemming is a normalization technique where list of tokenized words are converted into shorten root words to remove redundancy. Stemming is the process of reducing inflected (or sometimes derived) words to their word stem, base or root form.
A computer program that stems word may be called a stemmer.
A stemmer reduce the words like fishing, fished, and fisher to the stem fish. The stem need not be a word, for example the Porter algorithm reduces, argue, argued, argues, arguing, and argus to the stem argu .

Lemmatization
Major drawback of stemming is it produces Intermediate representation of word. Stemmer may or may not return meaningful word.
To overcome this problem Lemmatization comes into picture.
Stemming algorithm works by cutting suffix or prefix from the word.On the contrary Lemmatization consider morphological analysis of the words and returns meaningful word in proper form.
Hence,lemmatization is preferred.


POS (Part-Of-Speech) Tagging
POS (Parts of Speech) tell us about grammatical information of words of the sentence by assigning specific token (Determiner, noun, adjective , adverb ,verb,Personal Pronoun etc.) as tag (DT,NN ,JJ,RB,VB,PRP etc) to each words.
Word can have more than one POS depending upon context where it is used. we can use POS tags as statistical NLP tasks it distinguishes sense of word which is very helpful in text realization and infer semantic information from gives text for sentiment analysis.


Named Entity Recognition:
The process of recognizing named entity such as person name, location name , organization name , designation of person ,quantities or values.

Chunking (shallow parsing)
Chunking is the process of making a group of tokens into chunks. In simple words chunking is used as selecting the subsets of tokens. The parts of speech are combined with regular expressions.
Chunking is used for entity detection. An entity is that part of the sentence by which machine get the value for any intention
Chunking is used to categorize different tokens into the same chunk. The result will depend on grammar which has been selected. Further chunking is used to tag patterns and to explore text corpora.

Bag of Words (BoW) : Document Matrix
We cannot directly feed our text to machine learning algorithm; the text must be converted into vectors of numbers.
The bag-of-words model is method of feature extraction which preprocess the text by converting it into numeric format also known as vectors .BoW keeps count of the total occurrences of most frequently used words.
In simple terms, it’s a collection of words to represent a sentence with word count disregarding the order in which they appear.

Bag of Words just creates a set of vectors containing the count of word occurrences in the document , while the TF-IDF model contains information on the more important words and the less important ones as well.
Bag of Words vectors are easy to interpret. However, TF-IDF usually performs better in machine learning models.Hence TF-IDF is preferred.

TF-IDF :
TF-IDF stands for Term Frequency-Inverse Document Frequency
“Term frequency–inverse document frequency, is a numerical statistic that is intended to reflect how important a word is to a document in a collection or corpus.”
Term Frequency: is a scoring of the frequency of the word in the current document.
Inverse Document Frequency: is a scoring of how rare the word is across documents.

