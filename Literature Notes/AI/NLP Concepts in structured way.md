Tags: #nlp #ai
Author: Dhavan
Source: YT
Channel: CodeBasics

## Lecture 6

NLP
Explore methods other than regex
ML method, naive bayes = Spam detection

3 types -
	1 Rules and heuristic
	2 Naive bayes (Word vectorize) (ML)
	3 Sentence embedding (DL model)

text classification
	Vectorize text, send it into classifier to classify (naive bayes)

medical files in cloud, ocr or doc2vec to convert text into vector embedding and then classificatipn(linear regression classifier)

Facebook - Hate speech detection
LInkedIn - Fake peofiels

Cosine similarity


Information extraction
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250909185455.png)

Information retreival
Tiffin shops near me (Google)
return relevant websites
tfidif, bert

Chatbot
	FAQ bot
	Flow based bot (Develop conversation with you)
	Open ended bot (Normal conv)
Google translation (RNN)
Language modeslling: Auto complete
Statistic model and neural model
Text summerization 
Topic modelling (Retreive abstract topics)
Voice assistant
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250909190015.png)

NLP PIPELINE
**Data acquisation=> data cleaning => modeling => deploying => Monitoring

![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250909192349.png)

Naive bayes
vector embedding
bert
rnn 
ml codebasics
acc, precision, recall

CLassifying diff bw teaching and method abt naive bayes by stat quest and codr basics

!https://youtu.be/O2L2Uv9pdDA?si=DvmrWwChfyxuUmns
Stat Quest
bias: inability to caotyre true realtiion 
high biaas = basd
variance: how model performs on test fataset
lpw varianace = good
	low bias on train dataset but high variance => cause overfitting
3 things hel;p to fing sweet spit bw simple n comp mdiels regulatizstio;n, boosting bagging 

explore jadbio = justa add data automation ml
P(dear/Normal) = probability of word dear occurance in message normal
P(NNormall//dear friend) = likely hiood  of message normal if the word dear friend
![](/ZettleKasten/Unsorted/Attachment/Screenshot_20250909_202009.png)
lunch is not there in spam so it makes product zero to aviod it we use that black square bsically adding alpha to apply count

Naive bayes avoid grammar rules so it has high bias but low variance

**==Need to explor naive bias by code basics and link it back to nlp pipeline video link below n need tio summerixzae nlp video and write how I can apply for my hting==**

code basics nlp:
!https://youtu.be/S3EId9uatxI?si=5gMe9iIJy5s5q1r5

code basucs naive biaes:
!https://youtu.be/PPeaRc-r1OI?si=JRw7sRp3vP3ypu2i

JARGON used for feature engineering
explore tf-idf vectorize
One hot encoding
Word embedding 

---
### THings to explore


1) Gridsearch CV
2) [[Naive bias|Naive bayes]]
3) vector embedding
4) bert
5) rnn 
6) ml codebasics
7) acc, precision, recall
8) Deploy on cloud azure, google, aws
9) FastAPI 
10) Data bricks, amazon ssage maker, azure ml, h2o.ai
---


### NLP Lec - 7

![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250915060953.png)
Spacy automatically chooses the best algo available

Spacy is perfect for app developers

Nltk, we have the freedom to choose our own algo 

Nltk is perfect for researchers


Installation

```python
pip install spacy
python3 -m spacy download en
```

```python
pip install nltk
nltk.download('punkt')
```

---
### Lec - 8

WE will be using spacy in this course bcoz of the benefits mentioned above in the comparison.

!https://github.com/codebasics/nlp-tutorials/blob/main/4_tokenization/spacy_tokenizer_tutorial.ipynb\

```python
nlp = spacy.blank('en')
```

By using spacy.blank() we will get only tokenizer pipeline as shown below

![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250915064647.png)

```python
nlp = spacy.load('en_core_web_sm')
```

By using spacy.load() we will get the  entire pipeline as shown below

![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250915075926.png) ^4ec036

[NLP_practise](file:////home/sriram/Downloads/nlp/nlp.ipynb)

```python
dir(tokn)
```
This gives all possible methods an object or class can have
Eg:  Some of the imp methods
	1) is_alpha
	2) is_digit
	3) like_num
	4) is_currency
	5) is_punct
	6) like_email
	7) like_url

```python

from spacy.symbols import ORTH
nlp.tokenizer.add_special_case("gimme", [
    {ORTH: "gim"},
    {ORTH: "me"}
])
doc4 = nlp("gimme double cheese extra large healthy pizza")
tokens = [token.text for token in doc4]
print(tokens)
```

ORTH is used to create customized tokenizing rules (Only word splitting, not replacing)

```python
nlp.pipeline
nlp.add_pipe('sentencizer')
```

Used to add components in pipeline

---
### Lec 9

Need to summarize and write
pipeline - the [[NLP Concepts in structured way#^4ec036|components]] that comes after tokenizer in nlp
	token  => Individual tokens in a sentence
	token.pos_   => Parts  of speech
	token.lemma_  => Lemmatizer
	
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250917063714.png)

```python
nlp = spacy.load("en_core_web_sm")
nlp.pipeline

Output:

[('tok2vec', <spacy.pipeline.tok2vec.Tok2Vec object at 0x2170ce35280>),
('tagger', <spacy.pipeline.tagger.Tagger object at 0x2174163ec40>),
('parser', <spacy.pipeline.dep_parser.DependencyParser object at 0x2170a1953c0>),
('attribute_ruler',
<spacy.pipeline.attributeruler.AttributeRuler object at 0x2170c340c80>),
('lemmatizer', <spacy.lang.en.lemmatizer.EnglishLemmatizer object at 0x2170c333ac0>),
('ner', <spacy.pipeline.ner.EntityRecognizer object at 0x2170d03f200>)]
```

**Token, Parts of Speech, Lemmatization**

![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250917071835.png)

```python
doc = nlp("Captain america ate 100$ of samosa. Then he said I can do this all day.")

for token in doc:
print(token, "| ", token.pos_, "| ", token.lemma_)

Captain | PROPN | Captain
america | PROPN | america
ate | VERB | eat
100 | NUM | 100
```


**Demonstration of entities**
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250917043815.png)

```python
 doc = nlp("Tesla Inc is going to acquire twitter for $45 billion")
for ent in doc.ents:
print(ent.text, "|", ent.label_, "|", spacy.explain(ent.label_))


Tesla Inc | ORG | Companies, agencies, institutions, etc.
$45 billion | MONEY | Monetary values, including unit
```


**Name entity recognition in Frence**
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250917045209.png)

```python
nlp = spacy.load("fr_core_news_sm")
doc = nlp("Tesla Inc va racheter Twitter pour $45 milliards de dollars")
for ent in doc.ents:
 print(ent.text, " | ", ent.label_, " | ", spacy.explain(ent.label_))
Tesla Inc | ORG | Companies, agencies, institutions, etc.
Twitter | MISC | Miscellaneous entities, e.g. events, nationalities, products or works of art
```



**To make the appearance good and highlight**
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250917045141.png)

```python
from spacy import displacy
displacy.render(doc, style="ent")

Tesla Inc ORG is going to acquire twitter for $45 billion MONEY
```

**Used to add only the necessary pipelines from our source pipeline**
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250917065014.png)

```python
source_nlp = spacy.load("en_core_web_sm")
nlp = spacy.blank("en")
nlp.add_pipe("ner", source=source_nlp)
nlp.pipe_names

['ner']
```

Git hub link for lecture codes
!https://github.com/codebasics/nlp-tutorials/blob/main/5_spacy_lang_processing_pipeline/spacy_pipelines.ipynb

Git hub link for exercises
!https://github.com/codebasics/nlp-tutorials/blob/main/5_spacy_lang_processing_pipeline/language_processing_exercise.ipynb

---
### Lec 10

![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250917065833.png)

Spacy dont have stemming because it solely depends on lemmetization since it is more sophisticated

1. Now to practise we use NLTK
2. PorterStemmer, SnowballStemmer
3. token.lemma_  => Gives the base word
4. token.lemma => Returns unique hash of base  word 
5. attribute_ruler assigns attribute to particular token

**We can cstomise the attribute ruler rules by the below steps**
![](/ZettleKasten/Unsorted/Attachment/Pasted_image_20250917070810.png)
```python
ar = nlp.get_pipe('attribute_ruler')
ar.add([[{'TEXT': 'Bro'}],[{'TEXT': 'Brah'}]], [{'LEMMA': 'Brother'}])
doc = nlp("Bro, you wanna go? Brah, don't say no! I am exhausted")

for token in doc:
print(token.text, "|", token.lemma_)
```


Git hub link for lecture codes
!https://github.com/codebasics/nlp-tutorials/blob/main/6_stemming_lematization/6_stemming_lematization.ipynb

Git hub link for exercises
!https://github.com/codebasics/nlp-tutorials/blob/main/6_stemming_lematization/stemming_and_lemmatization_exercise.ipynb

---