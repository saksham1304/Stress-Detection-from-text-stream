# Stress Detection Using Text Classification

This project involves detecting stress in text data using Natural Language Processing (NLP) and machine learning techniques. The dataset used for this project is a CSV file (`Stress.csv`) containing text samples labeled as either stress-inducing or not.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Visualizations](#visualizations)
- [Prediction](#prediction)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/stress-detection.git
    cd stress-detection
    ```

2. Create and activate a virtual environment (optional but recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Place the `Stress.csv` file in the project directory.

2. Run the script:
    ```bash
    python stress_detection.py
    ```

3. Follow the on-screen instructions to input a text sample for stress prediction.

## Dataset

The dataset `Stress.csv` should have the following columns:
- `text`: The text sample.
- `label`: The label indicating whether the text is stress-inducing (1) or not (0).

## Data Preprocessing

The text data is preprocessed using the following steps:
- Convert text to lowercase.
- Remove text within square brackets.
- Remove URLs.
- Remove HTML tags.
- Remove line breaks.
- Remove words containing numbers.
- Remove punctuations.
- Tokenization and stemming using `SnowballStemmer`.

## Model Training and Evaluation

1. The preprocessed text data is split into training and test sets.
2. A `CountVectorizer` is used to transform the text data into feature vectors.
3. A `MultinomialNB` (Naive Bayes) classifier is trained on the training data.
4. The model is evaluated using accuracy, classification report, and confusion matrix.

### Results

- Accuracy: 0.75
- Classification Report:
    ```
              precision    recall  f1-score   support

           0       0.78      0.68      0.73       414
           1       0.73      0.82      0.77       438

    accuracy                           0.75       852
   macro avg       0.75      0.75      0.75       852
weighted avg       0.75      0.75      0.75       852
    ```

- Confusion Matrix:
    ```
    [[282 132]
     [ 81 357]]
    ```

## Visualizations

Word clouds are generated for stress and non-stress texts to visualize the most common words in each category.

![Word Clouds](wordclouds.png)

## Prediction

The model can predict if a given text indicates stress. Run the script and input your text when prompted to get a prediction.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

