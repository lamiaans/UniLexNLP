# UniLex NLP Project

NLP course project, Imam Abdulrahman Bin Faisal University
Section 9FA2, Group 1. Instructor: Dr. Hayat Alfaghum

## About
UniLex is our student-friendly dictionary for AI and CS terms. For this course we test one part of it: when a student asks a question in their own words, can the system tell which concept they mean?

We compare two methods on 16 concepts:
- Method 1: TF-IDF + Logistic Regression
- Method 2: Sentence-BERT (all-MiniLM-L6-v2) + Logistic Regression

Our question: which method finds the right concept more reliably?

The 16 concepts are Overfitting, Underfitting, Regularization, Dropout, Cross-validation, Gradient Descent, Learning Rate, Backpropagation, Tokenization, Stop Word, Stemming, Lemmatization, TF-IDF, Hallucination, Transfer Learning and Confusion Matrix.

## Results
Both methods were tested on the same 48 questions.

| Method | Correct | Accuracy | Macro F1 |
|---|---|---|---|
| TF-IDF + LR | 44/48 | 0.9167 | 0.9155 |
| SBERT + LR | 47/48 | 0.9792 | 0.9786 |

SBERT did better (1 mistake vs 4). But the test set is small (3 questions per concept), so the gap is only 3 questions and we can't say it is clearly better. Full results, confusion matrices and error analysis are in the notebook and the report.

## Files
- `UniLex_Comparison_CSV.ipynb` : the notebook
- `UniLex_Questions.csv` : the 320 questions
- `member_examples.csv` : 2 questions written by each member (tested separately)
- `requirements.txt` : packages we used
- `DATA_CARD.md` : where the data comes from
- `report/` : the final report (PDF)

## How to run
In Google Colab:
1. Upload the notebook.
2. Upload `UniLex_Questions.csv` and `member_examples.csv` to the same folder.
3. Click Runtime, then "Restart session and run all". It takes around 2 minutes.

On your own computer:
