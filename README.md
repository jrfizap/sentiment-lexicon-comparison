# Sentiment Lexicons Compared

VADER, AFINN, and TextBlob, three ready-made sentiment lexicons, labelling the same real comments as positive, negative, or neutral.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jrfizap/sentiment-lexicon-comparison/blob/main/notebooks/lexicon_sentiment_comparison.ipynb)

Individual coursework for CS190-2P, a third-year machine learning course at Mapúa Malayan Colleges Laguna, by Jherwin Indaya.

## Results

| Lexicon | Accuracy |
| --- | --- |
| VADER | **76%** |
| AFINN | 74% |
| TextBlob | 68% |

Scored on the first 50 comments of the dataset against their given labels. VADER did best, likely because it was built for short, informal social-media text.

## Method

- The lexicons are used as they are, with no training.
- **VADER:** positive when the compound score is at least 0.05, negative at −0.05 or below, neutral in between.
- **AFINN and TextBlob:** positive above zero, negative below, neutral at zero.
- Each prediction is compared with the comment's given label, and the notebook prints the per-comment scores for a few examples.

## Limits

With only 50 comments, the gaps between the three are small, and a different sample could reorder them.

## Repository contents

| Path | Contents |
| --- | --- |
| `notebooks/lexicon_sentiment_comparison.ipynb` | The three lexicons, per-comment predictions, and the accuracy comparison. Outputs are kept. |

The dataset is not included.

## How to run

1. Download the [Sentiment Analysis Dataset](https://www.kaggle.com/datasets/abdelmalekeladjelet/sentiment-analysis-dataset) from Kaggle.
2. Put `sentiment_data.csv` in your Google Drive's `MyDrive` folder.
3. Open the notebook with the **Open in Colab** badge above, run the cells in order, and allow the Drive mount when asked.

## License

The code and notebook are released under the [MIT License](LICENSE). The dataset keeps its own terms.
