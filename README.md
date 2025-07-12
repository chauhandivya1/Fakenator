# 📰 Fake News Generation and Detection using GPT-2 and BERT

This project demonstrates how to generate fake news using **GPT-2** and detect it using a fine-tuned **BERT** model. The approach highlights how the same AI technologies that can create misinformation can also be used to combat it.

> 🔗 [Original Google Colab Notebook](https://colab.research.google.com/drive/1l_Nc02KbxXaV-J6GwCT9NGLpmNIKfjVd)

---

## 📌 Features

- ✅ Generate believable fake news headlines with GPT-2
- ✅ Detect and classify news statements into 5 categories with BERT
- ✅ Uses the real-world **LIAR** dataset
- ✅ Includes preprocessing, fine-tuning, and evaluation
- ✅ Easy to run in Colab or locally

---

## 💡 Models Used

| Task | Model | Description |
|------|-------|-------------|
| Fake News Generation | [`gpt2`](https://huggingface.co/gpt2) | OpenAI GPT-2 for text generation |
| Fake News Detection | [`bert-base-uncased`](https://huggingface.co/bert-base-uncased) | BERT model fine-tuned for 5-class classification |

---

## 📊 Dataset

- **LIAR dataset** from UC Santa Barbara
- Contains 12.8k manually labeled political statements
- Download link: [liar_dataset.zip](https://www.cs.ucsb.edu/~william/data/liar_dataset.zip)

### Label Mapping:
| Label in Dataset | Mapped Value | Description |
|------------------|--------------|-------------|
| `false`, `pants-fire`, `pants on fire` | 0 | Fake |
| `barely-true`     | 1 | Weakly Fake |
| `half-true`       | 2 | Half True |
| `mostly-true`     | 3 | Mostly True |
| `true`            | 4 | Real |

---

## ⚙️ Installation

Run this in a Python environment (Colab or local):

```bash
pip install numpy==1.26.4 --force-reinstall
pip install --upgrade --force-reinstall transformers datasets torch torchvision
pip install evaluate
# Fakenator
