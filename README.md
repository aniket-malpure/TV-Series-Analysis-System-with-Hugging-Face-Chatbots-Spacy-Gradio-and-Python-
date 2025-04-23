# Analyze Your Favourite Series with NLP & LLMs

This project is a complete Natural Language Processing (NLP) and Large Language Model (LLM) powered system to **analyze your favorite series**, from dataset scraping to character chatbots. It combines modern AI techniques such as Named Entity Recognition, Zero-Shot Learning, and Transformer-based models, integrated into a user-friendly **Gradio web GUI**.

---

## Key Features

- **Custom Web Scraping**: Build your own dataset using Scrapy
- **Theme Classification**: Identify major themes using Zero-Shot Learning
- **Text Classification**: Fine-tuned LLM for multi-class classification of show content
- **Character Network**: Build an interactive graph of relationships using NER and NetworkX
- **Character Chatbot**: Talk to your favorite characters using an LLM-based chatbot
- **Gradio Interface**: Seamless web interface to explore all features

---

## Installation

```
git clone https://github.com/your-username/tv-series-nlp-project.git
cd tv-series-nlp-project
pip install -r requirements.txt
```

## Project Structure

- **crawler/**
  - Scrapes online sources to extract relevant episode, plot, and character information using Scrapy.
  - Output: A structured dataset (JSON/CSV) of dialogues, character metadata, and episode summaries.

- **theme_classifier/**
  - Uses Zero-Shot Classification (via Hugging Face Transformers) to identify thematic elements in text.
  - Model: facebook/bart-large-mnli or roberta-large-mnli
  - Example: Classifies an episode summary into themes like "revenge", "loyalty", "betrayal".

- **text_classifier/**
  - Custom multi-class classifier trained to categorize show content into genres, moods, or narrative elements.
  - Libraries: scikit-learn, transformers, or AutoTrain
  - Custom training pipeline supported (train/test splits, tokenizer, etc.)

- **character_network/**
  - Builds a character interaction graph using:
  - NER from spaCy to detect character names
  - NetworkX and PyVis for graph building and visualization
  - Shows who appears with whom, and how often (weighted edges)

- **charater_chat_bot/**
  - Create a chatbot to talk to characters using LLMs.
  - Model: Can be any dialogue-tuned transformer (like DialoGPT or Mistral)
  - Embeds character traits for more personalized responses
  - Ideal for fan engagement and immersive experience

- **gradio_app.py**
  - Hosts an interactive web GUI using Gradio. Integrates all modules into a central dashboard for easy use.
