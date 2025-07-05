# BBC News Classification Kaggle Mini-Project

This project explores methods for effectively classifying news articles, addressing the critical role of automated news classification in the digital era for quick and efficient access to information.

## Table of Contents

  * [Libraries Used](https://www.google.com/search?q=%23libraries-used)
  * [Data](https://www.google.com/search?q=%23data)
  * [Exploratory Data Analysis (EDA) and Data Preprocessing](https://www.google.com/search?q=%23exploratory-data-analysis-eda-and-data-preprocessing)
  * [Conclusion](https://www.google.com/search?q=%23conclusion)

## Libraries Used

The project utilizes the following key Python libraries:

  * `numpy`
  * `pandas`
  * `seaborn`
  * `matplotlib.pyplot`
  * `itertools`
  * `tqdm`
  * `wordcloud`
  * `nltk` (with `stopwords` downloaded)
  * `string`
  * `collections` (specifically `Counter`)
  * `sklearn` (for model selection, feature extraction, decomposition, linear models, SVM, pipelines, preprocessing, and metrics):
      * `train_test_split`
      * `GridSearchCV`
      * `TfidfVectorizer`
      * `NMF`
      * `LogisticRegression`
      * `TruncatedSVD`
      * `SVC`
      * `Pipeline`
      * `Normalizer`
      * `make_scorer`, `accuracy_score`, `confusion_matrix`, `ConfusionMatrixDisplay`

## Data

The project uses two primary datasets:

  * `BBC News Train.csv`: Training dataset with 1490 rows and 3 columns (`ArticleId`, `Text`, `Category`).
  * `BBC News Test.csv`: Test dataset with 735 rows and 2 columns (`ArticleId`, `Text`).

Both datasets were loaded using pandas, and an initial check confirmed no missing values in the training data.

## Exploratory Data Analysis (EDA) and Data Preprocessing

The EDA phase focuses on inspecting, visualizing, and cleaning the data:

  * **Data Inspection**: Initial checks include displaying the shapes, columns, and a few rows of both train and test datasets.
  * **Missing Values**: Verification of missing values in the training dataset revealed no missing entries.
  * **Category Distribution**: The distribution of categories in the news articles is visualized using a bar plot to understand data characteristics.
  * **Word Embedding Methods**: The notebook explores methods to process raw text into feature vectors. These include:
      * **TF-IDF**: Emphasizes important words while downweighting common ones.
      * **GloVe**: Captures semantic relationships between words using co-occurrence statistics.
      * **Word2Vec**: Generates word embeddings based on context using neural networks.
      * The project encourages referring to external resources (Kaggle discussions, research papers) for a deeper understanding of these NLP-specific techniques, as they were not covered in lectures.

## Conclusion

While both supervised and unsupervised approaches proved effective, supervised learning delivered the highest accuracy, making it the preferred method when labeled data is available. The strong performance of the unsupervised NMF model, however, underscores its value as a powerful alternative for text classification tasks where labeled data is limited or absent. Ultimately, the choice between these methods depends on the specific constraints and goals of the project. NMF excels in scenarios with limited data, while SVC demonstrates superior performance with sufficient training data, making both approaches valuable depending on the dataset and labeling constraints.