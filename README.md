<H3>NAME : THAANESH V</H3>
<H3>REGISTER NO : 212223230228</H3>
<H3>EX. NO.6</H3>
<H3>DATE: 28.10.2025</H3>
<H1 ALIGN =CENTER>Implementation of Semantic ANalysis</H1>
<H3>Aim: to perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques. </H3> 
 <BR>
<h3>Algorithm:</h3>
Step 1: Import the nltk library.<br>
Step 2: Download the 'punkt', 'wordnet', and 'averaged_perceptron_tagger' resources.<br>
Step 3:Accept user input for the text.<br>
Step 4:Tokenize the input text into words using the word_tokenize function.<br>
Step 5:Iterate through each word in the tokenized text.<br>
•	Perform part-of-speech tagging on the tokenized words using nltk.pos_tag.<br>
•	Print each word along with its corresponding part-of-speech tag.<br>
•	For each verb , iterate through its synsets (sets of synonyms) using wordnet.synsets(word).<br>
•	Extract synonyms and antonyms using lemma.name() and lemma.antonyms()[0].name() respectively.<br>
•	Print the unique sets of synonyms and antonyms.

## <H3>Program:</H3>
```python
!pip install nltk
import nltk

nltk.download( 'punkt_tab' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger_eng' )

sentence=input ()

tokens = word_tokenize(sentence)

pos_tags = nltk.pos_tag(tokens)

for word, tag in pos_tags:
print(word, tag)
from nltk.corpus import wordnet

synonyms =[]
antonyms =[]
for word in tokens:
for syn in wordnet.synsets(word) :
for lemma in syn.lemmas():
synonyms . append (lemma . name( ) )
if lemma . antonyms():
antonyms . append ( lemma. antonyms ( ) . name ( ) )

Print the synonyms and antonyms
print ( "Synonyms : " ,set (synonyms) )
print ( "Antonyms : " ,set(antonyms) )
```

<H3>Output</H3>
<img width="779" height="399" alt="image" src="https://github.com/user-attachments/assets/9e7ae7a2-9ddc-4864-95f5-a06bc55eec87" />

<img width="1480" height="54" alt="image" src="https://github.com/user-attachments/assets/c916f246-bc52-4826-909c-8ad6683713a9" />



<H3>Result:</H3>
Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.
