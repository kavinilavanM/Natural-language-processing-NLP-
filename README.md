# Natural-language-processing-NLP-
NLTK is a toolkit build for working with NLP in Python. It provides us various text processing libraries with a lot of test datasets. A variety of tasks can be performed using NLTK such as tokenizing, parse tree visualization, etc

"pip install nltk" to install the packages


Text Pre-Processing steps are followed below

* Tokenization
* Lower case conversion
* Stop Words
* Stemming
* Lemmatization
* bag of word

Tokenization - it is nothing but splitting up the paragraph into smaller part conveniently, it has two way of splitting word or sentence

syndex
word tokenizer
word_tokens = nltk.word_tokenize(text)
print (word_tokens)

sendence tokenizer
sent_token = nltk.sent_tokenize(text)
print (sent_token)

Lower case conversion - we have to convert upper case into lower case because it is case sensitive, For instance, He and he are different words
syndex
lower_text = text.lower()
print (lower_text)

stop words -meaningless or irrelevent words are stopword which we do not use . for instance , you , yourself, him etc
syndex
word_tokens = nltk.word_tokenize(text)
removing_stopwords = [word for word in word_tokens if word not in stopword]
print (removing_stopwords)

stemming-Stemming is a technique used to extract the base form of the words by removing affixes from them- for instance, final became fina
syndex
from nltk.stem import SnowballStemmer
word_tokens = nltk.word_tokenize(text)
stemmed_word = [snowball_stemmer.stem(word) for word in word_tokens]
print (stemmed_word)

Lemmatization technique is like stemming. The output we will get after lemmatization is called ‘lemma’, which is a root word rather than root stem
for instance went become go
syndex
lemmatized_word = [wordnet_lemmatizer.lemmatize(word) for word in word_tokens]
print (lemmatized_word)

bog - convert text into vector


