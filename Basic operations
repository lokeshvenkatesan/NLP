#NLP Program to demonstrate Tokenization ,Stemming ,Lemmatization , Bag of Words , POS ,Chunking
#Import libraries
import nltk
from nltk.tokenize import sent_tokenize, word_tokenize
from nltk.stem import PorterStemmer,LancasterStemmer
from nltk.stem import WordNetLemmatizer
from nltk.corpus import stopwords

#Sample Paragraph : Information about Manav Project
data="Recent times have witnessed an explosion in the amount of biological data generated. There are millions of research articles with pivotal information on human health and disease, spanning from single molecule resolution to the level of the whole organism. However, this information is scattered in different databases, repositories and in the text of journal articles. This makes the seamless extraction of scientific information an extremely challenging and time-consuming (yet incomplete) process. With 100+ databases and millions of data points (combined) from just human cells/tissue and disease, there is a pressing need to collate this information in such a way that users like academic/industrial/clinical researcher as well as teachers and students can easily access information that is relevant to them from a common and modular platform. Although there are ambitious ongoing efforts like the Recon X, The Virtual Physiological Human, Human Cell Atlas, none of these projects aim to build the map of the whole human body simultaneously comparing both macro(organ/tissue/cell) and micro (molecular interaction networks) level details. Manav-Human Atlas Initiative aims to construct a comprehensive map of the entire human body which will explicitly document macro to micro level information. The project Manav will dramatically accelerate our understanding of the working of the human body and help design better therapeutic targets for treating diseases like cancer, diabetes and more. This project will require understanding, extracting and collating information from millions of scientific papers which would need a massive investment of time, effort and manpower. The large pool of scientifically literate population in India pursuing a bachelors /masters / Ph.D. is a great resource that will be trained and engaged as part of this project to use the annotation tool being developed to collate, curate, manage and visualize this scientific information. This project is funded by Department of Biotechnology (DBT), Government of India as a collaboration between Persistent Systems, NCCS and IISER, Pune."

#STEP 1 :TOKENIZATION : Breaking complex data into simple units
#Sentence Tokenizer
sentences=sent_tokenize(data)
print(sentences)
#Word Tokenizer
words=word_tokenize(data)
print(words)

#Step 2: Stemming
#We are not using PorterStemmer as it produces intermediate words that don't have proper meaning
#Create object of PorterStemmer
#stemmer=PorterStemmer()
#Stemming with lemmatization to get proper meaning words after stemming
#Create obj of Lemmatizer
lemmmatizer=WordNetLemmatizer()

for i in range(len(sentences)):
    words=word_tokenize(sentences[i])
    #List comprehension
    #words=[stemmer.stem(word) for word in words if word not in set(stopwords.words('english'))]
    words = [lemmmatizer.lemmatize(word.lower()) for word in words if word not in set(stopwords.words('english'))]
    sentences[i]=' '.join(words)
print(sentences)

#Step 3 : Bag of Words : Document Matrix , Count Vectorizer
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x=cv.fit_transform(sentences).toarray()
print(x)

#TF-IDF
from sklearn.feature_extraction.text import TfidfVectorizer
cv=TfidfVectorizer()
x=cv.fit_transform(sentences).toarray()
print(x)
