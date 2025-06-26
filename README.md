# NLP Disaster Tweets Classification

This project applies Natural Language Processing (NLP) techniques to classify tweets as disaster-related or not. It uses pre-trained GloVe embeddings along with various deep learning models including Simple RNN, LSTM, and GRU for binary classification.

---

## Dataset

The dataset comes from the [Kaggle NLP with Disaster Tweets competition](https://www.kaggle.com/competitions/nlp-getting-started), which contains tweets labeled as:
- `1`: Related to a real disaster
- `0`: Not related to a disaster

---

## Project Highlights

- Data visualization and exploratory analysis (EDA)
- Text preprocessing:
  - URL removal
  - Lowercasing, punctuation and stopword removal
  - Tokenization and sequence padding
- Word embeddings using **GloVe** (`glove.6B.100d`)
- Training multiple deep learning models for classification

---

## Models Trained

| Model        | Embedding | Trainable | Description                     |
|--------------|-----------|-----------|---------------------------------|
| Simple RNN   | GloVe     | No        | Basic sequential model          |
| LSTM         | GloVe     | Yes       | Handles long-term dependencies  |
| GRU (basic)  | GloVe     | Yes       | Faster, simplified alternative  |
| GRU (tuned)  | GloVe     | Yes       | Added dropout and callbacks     |

---

## Evaluation

All models were trained using:
- Validation accuracy
- Validation loss
- Callback techniques such as EarlyStopping, ReduceLROnPlateau, and ModelCheckpoint to improve generalization

The best-performing model was the tuned GRU model, which showed strong performance and stability during training.

---

## Libraries Used

- TensorFlow / Keras
- NumPy, Pandas
- Matplotlib, Seaborn
- NLTK for text cleaning

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Shahwar0997/NLP-Disaster-Tweets.git
   cd NLP-Disaster-Tweets
   
