Statistical Language Modeling

A Statistical Language Modeling project built entirely from scratch using Python.
This project explores the foundations of Natural Language Processing (NLP) by implementing Unigram, Bigram, and Trigram language models using Maximum Likelihood Estimation (MLE), Add-k Smoothing, and Linear Interpolation. Model performance is evaluated using Perplexity, and the trained models are capable of generating realistic text through probabilistic sampling.

📖 Overview

Statistical Language Models estimate the probability of a sequence of words. They answer questions such as:

How likely is this sentence?
What is the most probable next word?

Before the rise of modern deep learning models such as GPT and BERT, statistical language models were the foundation of Natural Language Processing.

This project recreates these classic models completely from scratch without relying on machine learning libraries such as Scikit-Learn or TensorFlow. Every probability, smoothing technique, and evaluation metric is implemented manually to provide a deeper understanding of how language models work internally.

✨ Features
📚 Build Unigram, Bigram, and Trigram language models
📊 Estimate probabilities using Maximum Likelihood Estimation (MLE)
🧮 Implement Add-k (Laplace) Smoothing
🔄 Support Linear Interpolation between language models
📉 Evaluate models using Perplexity
✍️ Generate text through probabilistic sampling
📈 Explore vocabulary statistics and Zipf's Law
🧠 Handle unknown words using <unk> tokens
⚡ Fully implemented in pure Python
🧠 Understanding Statistical Language Models

A language model assigns a probability to a sequence of words.

Rather than memorizing complete sentences, an N-gram model estimates the probability of the next word based on the previous N − 1 words.

Using the Markov Assumption, the probability of a sentence becomes

P(w
i
	​

∣context)=
Count(context)
Count(context,w
i
	​

)
	​


where the counts are learned directly from a text corpus.

This project implements three different language models:

Model	Description
Unigram	Assumes every word is independent of previous words.
Bigram	Predicts a word based on the immediately previous word.
Trigram	Predicts a word using the previous two words.

Although simple compared to modern neural networks, N-gram models remain one of the best ways to understand:

Statistical NLP
Language Modeling
Smoothing
Probability Estimation
Perplexity
Text Generation
📂 Dataset

This project combines two well-known corpora available in the Natural Language Toolkit (NLTK).

Corpus	Description
Brown Corpus	Balanced corpus containing news, fiction, academic writing, government documents, and more.
Reuters Corpus	Financial news articles from Reuters.

Combined Statistics

Metric	Value
Total Sentences	111,812
Total Tokens	2,465,187
Vocabulary Size	57,611

During preprocessing the project

converts text to lowercase
removes non-alphanumeric tokens
replaces rare words with <unk>
pads sentences using <s> and </s>
📈 Corpus Exploration

Before training the models, the project explores the dataset by analyzing

Vocabulary Size
Word Frequencies
Rare Words
Hapax Legomena
Zipf's Law Distribution

The corpus follows Zipf's Law, where only a handful of words appear extremely frequently while the majority occur only a few times.

📊 Model Performance

Models were trained using an 80/20 Train-Test Split.

Performance was evaluated using Perplexity, where lower values indicate better predictive performance.

Model	Smoothing	Perplexity
Unigram	Add-k (1.0)	849.5
Unigram	Add-k (0.01)	849.0
Bigram	Add-k (1.0)	1200.7
Bigram	Add-k (0.01)	327.9
Trigram	Add-k (1.0)	5767.6
Trigram	Add-k (0.01)	1327.7
⭐ Interpolated Trigram	Linear Interpolation	227.0
🔍 Key Findings
✅ Context Matters

Including contextual information dramatically improves prediction accuracy. The Bigram model significantly outperforms the Unigram model because the previous word provides valuable context.

✅ Higher Order Isn't Always Better

A naive Trigram model performs worse than the Bigram because most trigram combinations never appear in the training corpus, resulting in data sparsity.

✅ Smoothing is Essential

Without smoothing, unseen word combinations receive zero probability, making the model unreliable on unseen data.
🛠️ Tech Stack
Python
NumPy
Matplotlib
NLTK
Jupyter Notebook
⚙️ Installation
git clone https://github.com/yourusername/statistical-language-modeling.git

cd statistical-language-modeling

pip install -r requirements.txt

python -m nltk.downloader brown reuters punkt punkt_tab
▶️ Getting Started

Run the notebooks in the following order:

01_corpus_exploration.ipynb
Corpus Statistics
Vocabulary Analysis
Zipf's Law
02_ngram_modeling.ipynb
Language Models
Perplexity Evaluation
Text Generation
📚 Skills Demonstrated

This project demonstrates practical experience with

Natural Language Processing (NLP)
Statistical Language Modeling
Probability Theory
Maximum Likelihood Estimation
Add-k Smoothing
Linear Interpolation
Perplexity Evaluation
Data Visualization
Python Programming
Object-Oriented Programming
🚀 Future Improvements
Kneser-Ney Smoothing
Good-Turing Smoothing
Beam Search Text Generation
Neural Language Models (LSTM)
Transformer-based Language Models
Interactive Streamlit Web Application

✅ Linear Interpolation Produces the Best Results

Combining Unigram, Bigram, and Trigram probabilities creates a more robust language model and achieves the lowest perplexity.

💜 Developed by Matthew Ferrer (Keigo)

Data Analytics • Data Science • Machine Learning • Natural Language Processing

"Building intelligent solutions through data, analytics, and artificial intelligence."
