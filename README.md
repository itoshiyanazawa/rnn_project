# Deep Learning Final Project: Text Generation with RNNs, LSTM, and GPT-2

This project explores various deep learning techniques for text generation using the Cornell Movie Dialogs Corpus. We evaluated character-level and word-level LSTM models, and fine-tuned a GPT-2 model for high-quality text generation.

## 📌 Objectives

- Compare character-level vs. word-level tokenization
- Experiment with LSTM architectures and training strategies
- Evaluate qualitative and quantitative performance
- Fine-tune a GPT-2 model for improved generation

## 🧠 Model Variants

- **Char-Level LSTM**: Embedding + LSTM + Dense
- **Word-Level LSTM**: Tokenizer + Embedding + LSTM + Dense
- **GPT-2 Fine-tuning**: Using `gpt_2_simple` on cleaned dialogue data

## 🧪 Evaluation Metrics

- **BLEU**, **ROUGE**, **Perplexity**, **Entropy**
- Qualitative scores on grammar, creativity, relevance, and diversity

## 🛠️ Tech Stack

- Python, TensorFlow, Keras, NLTK
- Google Colab, gpt_2_simple
- Matplotlib, visualkeras


## 🚀 Sample Output

> "i hope so you gonna leave it to be this way in the lateral part of the stomach"

## 📊 Evaluation & Results

We trained and evaluated three approaches using the Cornell Movie Dialogs Corpus:

| Model Type             | Tokenization     | BLEU    | ROUGE-1 / ROUGE-L | Perplexity | Entropy | Notes |
|------------------------|------------------|---------|--------------------|------------|---------|-------|
| Char-Level LSTM        | Character        | 2.7e-78 | 0.23 / 0.23        | 1289.07    | 5.29    | High repetition and incoherence |
| Word-Level LSTM        | Word             | 0.0000  | 0.25 / 0.25        | N/A        | 2.89    | Some syntactic improvement |
| GPT-2 Fine-tuned       | Word (GPT Token) | 0.1849  | 0.50 / 0.50        | N/A        | 3.91    | Coherent, fluent, diverse output |

### 📝 Observations:

- **Char-level LSTM** struggled to generate readable English, despite training improvements.
- **Word-level LSTM** showed better grammar and structure, but required significant data and compute.
- **GPT-2** (fine-tuned on the same corpus) achieved the best balance of coherence, creativity, and fluency with the lowest effort.

> "i hope so you gonna leave it to be this way in the lateral part of the stomach" – LSTM  
> "i'm not going to talk to you about that. i'm going to give you a call..." – GPT-2

### ⚖️ Conclusion

Fine-tuning GPT-2 was the most efficient and effective solution in both **qualitative** and **quantitative** terms. It outperformed LSTM-based models in coherence and contextual fluency, validating the benefit of transfer learning in NLP tasks under resource constraints.


## 🧾 Citation
> Chung et al. (2020). Rethinking embedding coupling in pre-trained language models. [arXiv:2010.12821](https://arxiv.org/abs/2010.12821)

---



