# Toxic Comment Classification with BERT for Wikishop

This project focuses on toxic comment classification for the Wikishop online store.

The goal is to build a machine learning model that can automatically classify user comments as **toxic** or **non-toxic**.

## Data

The project uses the `toxic_comments.csv` dataset with approximately **160,000 comments**.

| Column | Description |
|---|---|
| `text` | User comment text |
| `toxic` | Target label: toxic or non-toxic comment |

The dataset had no missing values or duplicates.
The target distribution was imbalanced: toxic comments accounted for about **10%** of the data.

## Workflow

The project included:

- exploratory analysis of user comments;
- text preprocessing;
- train/test split;
- training baseline models using TF-IDF;
- fine-tuning a lightweight BERT model;
- model evaluation using the F1 score.

## Models

Two approaches were compared:

### TF-IDF + Classical Models

The best classical model was:

**LinearSVC**

Results:

- Validation F1: **0.7952**
- Test F1: **0.7898**

Logistic Regression also showed strong performance:

- Validation F1: **0.7913**

### BERT

A lightweight BERT model, `bert-tiny`, was fine-tuned for text classification.

Results:

- Validation F1: **0.7810**
- Test F1: **0.7684**

## Results

The best overall solution was:

**TF-IDF + LinearSVC**

Although BERT achieved comparable results, it required significantly more training time and computational resources.

## Conclusion

For this task, the classical TF-IDF + LinearSVC approach provided the best balance between quality, speed, and simplicity.

BERT may be useful for further development, especially for more complex texts, multilingual data, or domain transfer. However, for the current dataset, **LinearSVC is the most practical solution**.

---

Created by [Christina Lebedeva](https://github.com/chris-lebedeva)
