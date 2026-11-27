## About

UniLex is our student-friendly dictionary for AI and CS terms. For this course we test one part of it: when a student asks a question in their own words, can the system tell which concept they mean?

We compare two methods on 16 concepts:

Method 1: TF-IDF + Logistic Regression
Method 2: Sentence-BERT (all-MiniLM-L6-v2) + Logistic Regression

Our question: which method finds the right concept more reliably?

The 16 concepts are Overfitting, Underfitting, Regularization, Dropout, Cross-validation, Gradient Descent, Learning Rate, Backpropagation, Tokenization, Stop Word, Stemming, Lemmatization, TF-IDF, Hallucination, Transfer Learning and Confusion Matrix.

Results

Both methods were tested on the same 48 questions.

Method	Accuracy	Macro F1
TF-IDF + LR	0.917	0.915
SBERT + LR	0.979	0.979

SBERT did better (1 mistake vs 4). But the test set is small (3 questions per concept), so we can't say it is clearly better. More details are in the notebook.

Files
UniLex_Comparison_CSV.ipynb : the notebook
UniLex_Questions.csv : the 320 questions
member_examples.csv : 2 questions written by each member (tested separately)
requirements.txt : packages we used
DATA_CARD.md : where the data comes from
docs/ : report and slides
How to run

In Google Colab:

Upload the notebook.
Upload UniLex_Questions.csv and member_examples.csv to the same folder.
Click Runtime, then "Restart session and run all". It takes around 2 minutes.

On your own computer:

pip install -r requirements.txt
jupyter notebook UniLex_Comparison_CSV.ipynb

Keep the two csv files in the same folder as the notebook.

Try it

The "Try it" section has a function try_it("your question"). It shows what both models predict, without training again. If you give it an empty text it tells you to enter a question.

Data
80 questions are real titles from Stack Exchange (Data Science, Cross Validated, Stack Overflow, AI). Links and authors are in the csv.
240 questions were written with Claude's help and checked by our team.

The test set only uses the real Stack Exchange questions. Train, dev and test do not share any questions. We picked the settings on the dev set only, seed = 42.

Credits
Stack Exchange questions (CC BY-SA)
Sentence-BERT paper: Reimers and Gurevych, 2019
BERT paper: Devlin et al., 2019
scikit-learn and the sentence-transformers library
Claude (Anthropic) helped write the AI-assisted questions
Team

Sara Mousa Almousa (leader), Tala Abdullah Alghamdi, Lamya Khalid Alansari, Samar Ali Alyami
