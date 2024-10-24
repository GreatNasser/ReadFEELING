# Emotion Tracker with AI Sentiment Analysis

## Overview
Welcome to **Emotion Tracker**, an AI-powered app designed to analyze and track your emotions based on daily journal entries. With this app, you can monitor your emotional well-being over time and gain insights into your mood patterns.

## Key Features
- **🧠 AI-Based Sentiment Analysis**: Automatically analyzes your text to classify your emotions as positive, negative, or neutral.
- **📊 Visual Mood Tracking**: Interactive graphs that show your emotional fluctuations over days, weeks, or months.
- **🔔 Daily Reminders**: Never miss a day of journaling with helpful notifications to encourage consistent usage.
- **💡 Insights and Suggestions**: Provides recommendations based on your emotional state to improve your well-being.
- **🌐 Integration with Wellness Apps**: Seamlessly connects with popular mental health apps like **Headspace** and **Calm** to offer personalized mindfulness exercises.

## Installation Guide

Follow these steps to install and run the application locally:

1. **Install Python** (version 3.7 or higher) from [python.org](https://www.python.org/downloads/).
   
2. **Clone the Repository**:
   ```bash
   git clone https://github.com/GreatNasser/EmotionTracker.git
   cd EmotionTracker
pip install nltk textblob flask matplotlib
python app.py
http://127.0.0.1:5000
from textblob import TextBlob

text = """
The titular threat of The Blob has always struck me as the ultimate movie
monster: an insatiably hungry, amoeba-like mass able to penetrate
virtually any safeguard, capable of--as a doomed doctor chillingly
describes it--"assimilating flesh on contact.
Snide comparisons to gelatin be damned, it's a concept with the most
devastating of potential consequences, not unlike the grey goo scenario
proposed by technological theorists fearful of
artificial intelligence run rampant.
"""

blob = TextBlob(text)
blob.tags  # [('The', 'DT'), ('titular', 'JJ'),
#  ('threat', 'NN'), ('of', 'IN'), ...]

blob.noun_phrases  # WordList(['titular threat', 'blob',
#            'ultimate movie monster',
#            'amoeba-like mass', ...])

for sentence in blob.sentences:
    print(sentence.sentiment.polarity)
# 0.060
# -0.341
