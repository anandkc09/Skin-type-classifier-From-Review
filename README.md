# 🧴 Skin Type Classifier from Customer Reviews

A Machine Learning project that predicts a user's **skin type** from customer review text using **Natural Language Processing (NLP)** and a trained classification model.

## 📌 Project Overview

This project analyzes customer reviews and uses text-based machine learning to identify the skin type mentioned in the review.

The project uses **TF-IDF (Term Frequency–Inverse Document Frequency)** for converting review text into numerical features and a trained machine learning classifier for prediction.

### 🎯 Objective

The main objective is to automatically identify skin types such as:

- Dry Skin
- Oily Skin
- Combination Skin
- Sensitive Skin
- Normal Skin

This can help skincare recommendation systems understand customer needs from their written reviews.

---

## 🧠 Machine Learning Pipeline

```text
Customer Review
      ↓
Text Preprocessing
      ↓
TF-IDF Vectorization
      ↓
Trained ML Classifier
      ↓
Predicted Skin Type
```

---

## 📂 Repository Structure

```text
Skin-type-classifier-From-Review/
│
├── models/
│   ├── skin_type_classifier.joblib
│   └── tfidf_vectorizer.joblib
│
└── README.md
```

### Model Files

**`skin_type_classifier.joblib`**

Contains the trained machine learning classification model.

**`tfidf_vectorizer.joblib`**

Contains the fitted TF-IDF vectorizer used to transform review text into numerical features.

Both files are required to make predictions on new reviews.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- TF-IDF
- Joblib
- Jupyter Notebook
- Natural Language Processing (NLP)
- Git & GitHub

---

## 💻 Installation

Clone the repository:

```bash
git clone https://github.com/anandkc09/Skin-type-classifier-From-Review.git
```

Move into the project folder:

```bash
cd Skin-type-classifier-From-Review
```

Install the required libraries:

```bash
pip install pandas numpy scikit-learn joblib
```

---

## 🚀 How to Use the Model

Load the trained model and TF-IDF vectorizer:

```python
import joblib

model = joblib.load("models/skin_type_classifier.joblib")
vectorizer = joblib.load("models/tfidf_vectorizer.joblib")
```

Enter a customer review:

```python
review = ["My skin feels very dry and needs a lot of moisturizer."]
```

Transform the review using the TF-IDF vectorizer:

```python
review_vector = vectorizer.transform(review)
```

Make the prediction:

```python
prediction = model.predict(review_vector)

print("Predicted Skin Type:", prediction[0])
```

---

## 📊 Example

### Input

```text
"My skin gets very oily after a few hours and I often get acne."
```

### Output

```text
Predicted Skin Type: Oily Skin
```

---

## 🔍 Key Features

- 📝 Extracts information from customer reviews
- 🔤 Uses NLP-based text processing
- 📊 Converts text into numerical features using TF-IDF
- 🤖 Uses a trained ML classification model
- 💾 Saves the trained model using Joblib
- 🔄 Can be integrated into a skincare recommendation system

---

## 🌟 Future Improvements

- Improve prediction accuracy with a larger labeled dataset
- Add more skin-related categories
- Perform advanced NLP preprocessing
- Compare multiple ML algorithms
- Add confidence scores for predictions
- Build a web application using Flask or Streamlit
- Integrate the classifier with a skincare recommendation system

---

## 👨‍💻 Author

**Anandkumar Chaurasiya**

B.Tech Artificial Intelligence & Machine Learning

GitHub:  
https://github.com/anandkc09

---

## 📄 License

This project is created for educational, research, and portfolio purposes.
