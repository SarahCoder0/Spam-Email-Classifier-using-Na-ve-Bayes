# Spam-Email-Classifier-using-Na-ve-Bayes
A machine learning project to detect spam emails with high accuracy. Leveraging **Naïve Bayes** for text classification and **OpenAI Whisper** for voice input, the system supports both written and spoken messages. Built with Python and Streamlit for an interactive user interface.

---

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [AI Component](#ai-component)
- [Performance](#performance)
- [License](#license)

---

##  Overview
Spam emails are a major digital nuisance. This project develops a classifier to automatically detect spam, providing a reliable solution for email filtering. Integration with **OpenAI Whisper** allows voice messages to be transcribed and classified, enhancing accessibility.

---

##  Dataset
- Source: **Kaggle Spam Email Dataset**.
- Size: 5,728 labeled emails.
- Features:
  - `text`: Email content.
  - `spam`: Label (1 = spam, 0 = not spam).

---

##  Methodology
1. **Data Preprocessing:** Shuffling, lowercasing, punctuation removal, tokenization, stopword removal (NLTK), TF-IDF feature extraction.  
2. **Model Development:** Multinomial Naïve Bayes with Laplace smoothing (α=0.03) for text classification. Random Forest tested for comparison.  
3. **Evaluation:** Metrics include accuracy, precision, recall, and F1-score.

---

## 🤖 AI Component
- **Whisper:** Pre-trained speech-to-text model from OpenAI. Transcribes audio messages (.m4a) into text for classification.  
- **Why Whisper:** Multilingual, robust to noise, easy to integrate, no fine-tuning needed.

---

## Performance

**Naïve Bayes:**  
- Accuracy: 98.87%  
- Precision: Not Spam 0.99, Spam 0.99  
- Recall: Not Spam 1.00, Spam 0.97  
- F1-score: Not Spam 0.99, Spam 0.98  
- Observations: High accuracy and balanced performance; effective in detecting both spam and not-spam messages.

**Random Forest (for comparison):**  
- Accuracy: 97.82%  
- Precision: Not Spam 0.97, Spam 1.00  
- Recall: Not Spam 1.00, Spam 0.91  
- F1-score: Not Spam 0.99, Spam 0.95  
- Observations: High precision for spam, slightly lower recall, less balanced than Naïve Bayes.

**Latency:** 2–3 seconds per classification.  
**Conclusion:** Naïve Bayes is the preferred model due to balanced, high performance.

---

## License
This project is for **showcase purposes only**. Reproduction, modification, or commercial use without explicit permission is prohibited.
