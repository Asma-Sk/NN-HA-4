# NN-HA-4
1 Sol :
  1. 1.	Difference between stemming and lemmatization (Example: “running”):
Stemming:
Rough chopping to reduce a word to its root form.
Example: "running" → "run"
Lemmatization:
Linguistically correct form based on dictionary rules.
Example: "running" → "run" (but if it was "better", lemmatization would change it to "good", not just chop it.)
 Stemming is faster but cruder. Lemmatization is slower but smarter.
2. 
Removes noise (e.g., "the", "is", "in") to focus on meaningful words.
Improves performance in tasks like topic modeling, document clustering.
Harmful:
In tasks like sentiment analysis or question answering, stop words like "not" are important.
Example:
"I do not like pizza." → If "not" is removed, meaning flips completely!

2 Sol :
  1. 1.	How does NER differ from POS tagging?
Aspect	Named Entity Recognition (NER)	Part-of-Speech (POS) Tagging
Purpose	Identify real-world entities (names, places, dates)	Identify grammatical roles (noun, verb, adjective)
Example Output	"Barack Obama" → PERSON	"served" → VERB, "President" → NOUN
Focus	Meaning and category of phrases	Grammatical function of words
 In short:
•	POS tagging = Grammar role
•	NER = Real-world object recognition
2.	Two applications using NER:
a) Financial News Analysis
Automatically detect companies, stock names, people, and dates from articles.
Example: "Tesla shares dropped after Elon Musk's announcement" → [Tesla → ORG], [Elon Musk → PERSON].

b) Search Engines (like Google)
Improve search relevance by recognizing entities.
If someone searches "movies directed by Christopher Nolan", it detects [Christopher Nolan → PERSON] and fetches targeted results.
/89+6

3 Sol :
  1. 
1.	Why do we divide the attention score by √d?
 The dot-product between Q and K can become very large if the dimension d is big.
Very large values passed into softmax cause extremely small gradients during training (because softmax saturates). Dividing by √d stabilizes the gradients and keeps the softmax values reasonable.
 Summary:
To avoid exploding values and make training stable.

2.	How does self-attention help the model understand relationships between words?
Self-attention allows the model to look at all words in a sentence when encoding a single word.
 Example:
In "The cat sat on the mat", when processing "sat", the model can "attend" to "cat" and "mat" to better understand context.
 This helps capture:
Long-distance relationships (important in complex sentences)
Semantic meaning (subject-verb agreements, etc.)
 Summary:
Self-attention lets each word understand its context by looking at every other word, making meaning richer!


4 Sol :
  1. 1.	What is the main architectural difference between BERT and GPT?
 BERT uses only the encoder part of the Transformer architecture. GPT uses only the decoder part of the Transformer.
Model	Architecture	Direction
BERT	Encoder	Bidirectional (reads left and right)
     GPT	Decoder	Unidirectional (reads left-to-right for generation)
 Summary:
BERT is for understanding (encoding meaning), GPT is for generating (decoding into text).

2. 
Why is using pre-trained models (like BERT or GPT) beneficial for NLP applications?
 Massive Data: Pre-trained models are trained on huge datasets (Wikipedia, books, web pages).

 Save Time and Resources: Training from scratch would need tons of GPUs and weeks/months.

 Better Generalization: Pre-trained models learn rich language patterns that can transfer to many tasks (sentiment, translation, QA).

 Summary:
Pre-trained models give you powerful language understanding/generation without spending huge compute and time!



