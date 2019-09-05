# DebatesTopicModeling
![Debates Topic Modeling](images/Presidential_Debates_NLP_Analysis_Topic_Modelling.png "Debates Topic Modelling")

## Purpose
Over  40 years Democrats and Republicans have developed ways to reach their base with specialized language and issues. Using Machine Learning tools I analyzed Presidential Debates Transcripts and compared Democrats and Republicans when they are asked the same straight questions under the same venue and analyzed how they responded differently.

## The Data
Debates are the chosen dataset because of the common venue and equavalent time given to each topic. The pro's to this approach are the clear equivalencies both between candidates and over time. The topics even from election to election to not vary wildly. (eg. Foreign Policy will come up in every election but in different contexts). The cons the dataset is small. The topics are heavily moderated, so it is dificult for the candidates to differentiate themselves.
- The Presidential Debate Transcripts 1960-2016
Every 4 years three debates with 1 Democrat and 1 Republican presidential candidate
Nixon refused to debate 1964 and 1968  
- One Vice Presidential debate each election  
- 42 speeches total.
- 7317 spoken lines of dialogue.

## Natural Language Processing toolkits  
- NLTK - word tokenizer, stop words.
- SpaCy - tagger, parser, lemmatizer.
- Gensim - LDA Topic Modelling.
- SKLearn - Vectorizor, TFIDF
- VADER - Sentiment Analysis

## The Direct Comparison - Machine Learning Models
The first line of attack is modelling each line of dialogue as Democrat-spoken or Republican-spoken. This is done after tokenizing and lemmatizing each speech particle and having the machine learning model pick out the meaningful differences. For example, 'abortion' and 'life' are repeated among Republicans and 'choice' is repeated more among Democrats. Using this as a baseline we can get an idea of how accurately a line selected at random can be meaningfully attributed to a Democrat or a Republican.

We use accuracy as the metric of choice because the balance of datapoints is equivalent between the two parties so we just want to know the most informed model. The top accuracy score is 68%. Good, not great.

## The Breakdown of Topics - Gensim Topic modelling
We can find out what the candidates spend their time talking about by topic. For this we are using Gensim topic modelling with TFIDF. 
