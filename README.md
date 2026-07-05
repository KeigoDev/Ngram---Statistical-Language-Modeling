## 🧠 Statistical Language Modeling
Building Classic N-Gram Language Models from Scratch with Python
<p align="center">










</p>
## 📌 Overview

Statistical Language Modeling is one of the fundamental techniques in Natural Language Processing (NLP). Before the emergence of transformer-based models like GPT, language understanding relied heavily on probability theory and word statistics.

This project implements the complete pipeline of a statistical language model from scratch using Python. Instead of relying on machine learning frameworks, every probability calculation, smoothing algorithm, and evaluation metric is manually implemented to demonstrate the underlying mathematics behind language modeling.

## 🎯 Project Objectives

✔ Build Unigram, Bigram, and Trigram language models

✔ Estimate word probabilities using Maximum Likelihood Estimation (MLE)

✔ Handle unseen words using Add-k Smoothing

✔ Improve predictions using Linear Interpolation

✔ Evaluate models using Perplexity

✔ Generate realistic text through probabilistic sampling

✔ Analyze corpus statistics and Zipf's Law

## 📚 Dataset

The project combines two benchmark corpora from NLTK.

Dataset	Description
Brown Corpus	Balanced English corpus covering news, fiction, government, and academic writing
Reuters Corpus	Financial and business news articles
Combined Statistics
Metric	Value
Sentences	111,812
Tokens	2,465,187
Vocabulary	57,611

## 🧠 Language Models
Model	Context
Unigram	Predicts words independently
Bigram	Uses one previous word
Trigram	Uses two previous words
Interpolated Trigram	Combines Uni + Bi + Tri probabilities
📈 Results
Model	Perplexity ↓
Unigram	849.0
Bigram	327.9
Trigram	1327.7
## ⭐ Interpolated Trigram	227.0

Lower perplexity indicates a better language model.

## 🔬 What I Learned

Through this project I gained practical experience with:

Statistical Language Modeling
Natural Language Processing
Probability Theory
Maximum Likelihood Estimation
Add-k Smoothing
Linear Interpolation
Perplexity Evaluation
Corpus Analysis
Zipf's Law
Object-Oriented Programming

## ⚙️ Installation

cd statistical-language-modeling

pip install -r requirements.txt

python -m nltk.downloader brown reuters punkt punkt_tab
🚀 Running the Project
jupyter notebook


## 💻 Technologies Used
- Python
- NumPy
- Matplotlib
- NLTK
- Jupyter Notebook
## 🌱 Future Improvements
Kneser-Ney Smoothing
Good-Turing Smoothing
Beam Search
LSTM Language Models
Transformer Language Models
Streamlit Interactive Demo

##👨‍💻 Author
##Matthew Ferrer (Keigo)

Data Analytics • Data Science • Machine Learning • Natural Language Processing

"Learning AI by understanding the mathematics that power intelligent systems."

⭐ Support

If you found this project helpful or interesting, consider giving it a ⭐ Star on GitHub!
