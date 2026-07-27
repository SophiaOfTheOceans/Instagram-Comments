### Overview

This project was completed as the Georgia Tech MS Analytics Practicum in partnership with **Optimize Social**.

Traditional social media dashboards report metrics such as likes, comments, and reach but provide little insight into **why audiences engage**. This project transforms Instagram comments into structured, creator-specific audience intelligence using NLP, machine learning, and LLMs.

The objective was to answer questions such as:

* What are followers asking for?
* Which comments indicate purchase intent?
* What content generates confusion?
* Which topics drive positive engagement?
* What recommendations can creators act on?

---

## Dataset

* 34,881 Instagram comments
* 473 posts
* 66 creator accounts

Each post included metadata such as

* Caption
* Creator
* Topic
* Media type
* Likes
* Views
* Timestamp

Comments were originally stored as raw text blocks and first had to be parsed into individual comment records.

---

## Methods

### Data Processing

* Parsed raw comment blocks into comment-level records
* Cleaned usernames and formatting artifacts
* Engineered creator- and post-level features

### Intent Classification

Compared three different approaches:

1. Rule-based regex classifier
2. Sentence-BERT embeddings + Logistic Regression
3. GPT-4.1 Mini

Target labels included

* Questions
* Requests
* Purchase intent
* Confusion
* Pain points

---

### Sentiment Analysis

* VADER
* GoEmotions (BERT)

---

### Topic Analysis

* TF-IDF
* Sentence Transformer embeddings
* K-Means clustering
* GPT topic extraction

---

### Creator Analytics

Built creator-level metrics including

* FAQ generation
* Purchase-intent summaries
* Confusion detection
* Viral-adjusted topic performance
* Audience opportunity summaries

---

## Technologies

* Python
* Pandas
* NumPy
* scikit-learn
* Sentence Transformers (SBERT)
* OpenAI GPT-4.1 Mini
* VADER
* GoEmotions
* NLTK
* Matplotlib

---

## Key Results

* Processed **34K+ comments** into structured analytics.
* Demonstrated that **LLM-based classification produced the most contextually accurate results**, while rule-based methods offered interpretability and embedding-based models balanced performance with cost.
* Developed creator-specific recommendation outputs that moved beyond engagement reporting to actionable audience insights.
* Produced a workflow suitable for future integration into creator dashboards and analytics products.

---

## Future Improvements

* Fine-tune embedding models with additional labeled data.
* Improve prompt engineering for topic extraction.
* Evaluate additional LLMs (Claude, GPT-4.1, Gemini).
* Build an interactive dashboard for creator insights.
* Validate classifications against larger human-labeled datasets.
