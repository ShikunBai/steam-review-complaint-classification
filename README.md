# Multi-label Classification of Complaint Types in Steam Reviews

MA3831 Assessment 3 (WebCrawler and NLP System), Shikun Bai.

English Steam reviews were scraped from the Steam Community with BeautifulSoup, cleaned, labelled with 7 complaint types (multi-label) and used to compare a TF-IDF + logistic regression baseline with TextCNN and BiLSTM models initialised with Word2Vec or random embeddings. Data are split by game, so the 3 test games are unseen during training.

## Test results (600 hand-labelled reviews, 3 unseen games)

| Model | micro-F1 | macro-F1 | Log loss |
|:---|:---|:---|:---|
| TF-IDF + LR | 0.688 | 0.588 | 0.399 |
| TextCNN-W2V (main) | 0.680 ± 0.019 | 0.643 ± 0.014 | 0.381 ± 0.017 |
| TextCNN-Random | 0.616 ± 0.007 | 0.572 ± 0.013 | 0.432 ± 0.010 |
| BiLSTM-W2V | 0.667 ± 0.009 | 0.628 ± 0.015 | 0.421 ± 0.017 |
| BiLSTM-Random | 0.623 ± 0.020 | 0.585 ± 0.020 | 0.468 ± 0.023 |

Neural models: mean ± sd over 5 seeds.

## Repository contents

| Path | Contents |
|:---|:---|
| `notebooks/A3_Shikun_Bai.ipynb` | The full pipeline: game selection, scraping, cleaning, sampling, labelling checks, Word2Vec, models, validation and test evaluation |
| `report/A3_Shikun_Bai.pdf` | Written report |
| `labelling/` | Codebook, LLM prompt, LLM answers (review IDs and labels only) and the annotator manifest |
| `outputs/` | Configurations, aggregate tables, figures, predicted probabilities, the Word2Vec model, the baseline model and the final TextCNN and BiLSTM models (5 seeds each) |

## Data not included

Review text is not published. The raw scraped reviews, the cleaned review files, the labelled sample with text, the embedding corpus, the hand-labelling workbook and the salt used to hash review links are excluded. Review IDs (`label_id`) and salted hashes (`review_key`) contain no user identity.

## Running the notebook

The notebook keeps the outputs of the original runs; scraping and training are not re-run. The code expects the repository folder to be named `A3` and the notebook to be run from `A3/notebooks`, for example:

```bash
git clone https://github.com/ShikunBai/steam-review-complaint-classification.git A3
```

Steps that need the excluded review files will not run without re-scraping, and Steam pages change over time, so a new scrape will not reproduce the same corpus. Python 3.13.9 was used; package versions are in `requirements.txt`.
