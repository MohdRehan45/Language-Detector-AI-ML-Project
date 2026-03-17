**🌍 Language Detection using Naive Bayes (Machine Learning)**

**📌 Project Overview**

This project implements a Language Detection System using Machine Learning in Python. The model automatically predicts the language of a given text using the Multinomial Naive Bayes algorithm and Bag-of-Words feature extraction.

Language detection is an important task in Natural Language Processing (NLP) and is widely used in:

Translation systems

Search engines

Chatbots

Content filtering

Social media analysis

This project demonstrates how text data can be converted into numerical features and classified into multiple languages using a supervised machine learning model.

**🧠 Machine Learning Concepts Used**

This project uses several fundamental machine learning and NLP techniques.

**1️⃣ Bag of Words (BoW)**

The text data is converted into numerical form using CountVectorizer.

Bag of Words counts the frequency of each word in a sentence.

Example:

Text Data

"I love data science"
"I love machine learning"

Vocabulary

['data', 'learning', 'love', 'machine', 'science']

Vector Representation

Sentence	data	learning	love	machine	science
love data science	1	0	1	0	1
love machine learning	0	1	1	1	0

This numerical representation allows machine learning models to process text data.

2️⃣ Multinomial Naive Bayes

The project uses the Multinomial Naive Bayes classifier, which is widely used for text classification problems such as:

Spam detection

Sentiment analysis

Language identification

Document classification

Naive Bayes works on probability theory and assumes that features (words) are independent.

Advantages:

Fast

Efficient for text data

Works well with large vocabularies

**📂 Dataset Description

The dataset used in this project contains sentences from multiple languages.

Dataset Features:

Column	Description
Text	Sentence or paragraph
Language	Language label

Example:

Text	Language
"Bonjour tout le monde"	French
"Hola amigo"	Spanish
"你好"	Chinese

Dataset Statistics:

22 languages

1000 samples per language

22000 total samples

Languages included:

English

Hindi

Tamil

Chinese

Arabic

Spanish

French

Russian

Korean

Japanese

Turkish

Urdu

Persian

Estonian

Swedish

Romanian

Portuguese

Indonesian

Dutch

Thai

Latin

Pushto

The dataset is balanced, meaning each language has an equal number of samples.

**⚙️ Project Workflow**

The complete pipeline of the project follows these steps:

1️⃣ Import Required Libraries

The project uses:

pandas

numpy

scikit-learn

These libraries are used for data processing, feature extraction, and model training.

2️⃣ Load Dataset

The dataset is loaded using pandas:

df = pd.read_csv("language.csv")

The dataset contains text samples and their corresponding language labels.

3️⃣ Data Preprocessing

Basic preprocessing steps include:

Checking for missing values

Inspecting class distribution

Extracting features and labels

4️⃣ Text Vectorization

Text is converted into numerical features using CountVectorizer.

cv = CountVectorizer()
X = cv.fit_transform(x)

This step transforms text into a Bag-of-Words matrix.

5️⃣ Train-Test Split

The dataset is split into training and testing sets.

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.33, random_state=42
)

67% training data

33% testing data

6️⃣ Model Training

The Multinomial Naive Bayes model is trained using the training dataset.

model = MultinomialNB()
model.fit(X_train, y_train)
7️⃣ Model Evaluation

The model performance is evaluated using accuracy.

model.score(X_test, y_test)

Result:

Accuracy ≈ 95%

This indicates the model correctly predicts the language for most samples.

8️⃣ Language Prediction

The trained model can predict the language of any input text.

Example:

user = input("Enter a Text: ")
data = cv.transform([user]).toarray()
output = model.predict(data)

print(output)

Example Input:

你好

Output:

Chinese
📊 Project Results

Model Accuracy:

95.31%

The model performs well because:

Balanced dataset

Large training data

Effective text representation

Suitable classification algorithm

**💻 Technologies Used**

Python

Pandas

NumPy

Scikit-learn

Natural Language Processing (NLP)

**🚀 Applications**

This project can be extended and used in real-world systems such as:

Google Translate type systems

Chatbots

Content moderation

Multilingual document classification

Automatic language detection for websites

**🔮 Future Improvements**

Possible improvements include:

Using TF-IDF vectorization

Applying Deep Learning models

Using LSTM or Transformer models

Adding more languages

Creating a web application using Flask or Streamlit

**📌 Conclusion**

This project demonstrates how machine learning and natural language processing techniques can be used to automatically detect the language of text. Using CountVectorizer and Multinomial Naive Bayes, we achieved high accuracy with a simple and efficient model.

The project serves as a strong beginner-friendly NLP project and can be expanded into more advanced language detection systems.
