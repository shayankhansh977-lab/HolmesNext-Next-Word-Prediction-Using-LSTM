# HolmesNext – Next Word Prediction Using LSTM

## Project Overview

HolmesNext is an NLP (Natural Language Processing) based project that predicts the next word of a given sentence using a Deep Learning model called LSTM (Long Short-Term Memory).

This model is trained on the book **The Adventures of Sherlock Holmes** by Arthur Conan Doyle. It learns patterns and relationships between words from the book and uses those patterns to predict the next possible word.

Users can enter a sentence, and the model predicts one word that is likely to come next.

## Features

- Text preprocessing and cleaning
- Sentence tokenization
- Word lemmatization using NLTK
- Text tokenization using Keras Tokenizer
- N-gram sequence generation
- Sequence padding
- LSTM-based deep learning model
- Next-word prediction from user input
- Interactive prediction interface

## Technologies Used

- Python
- TensorFlow
- Keras
- NLTK
- NumPy
- Pandas
- Scikit-learn
- Google Colab

## Dataset

**Dataset Name:** The Adventures of Sherlock Holmes

**Author:** Arthur Conan Doyle

**Format:** TXT (Text File)

The dataset contains the text of Sherlock Holmes stories and is used to train the next-word prediction model.

## Model Architecture

The project uses an LSTM-based neural network.

| Layer | Configuration |
|---|---|
| Input Layer | Fixed-length sequences |
| Embedding Layer | 128 dimensions |
| LSTM Layer 1 | 128 units |
| LSTM Layer 2 | 64 units |
| Output Layer | Dense + Softmax |

### Model Compilation

- **Optimizer:** Adam
- **Loss Function:** Sparse Categorical Crossentropy
- **Evaluation Metric:** Accuracy
- **Epochs:** 10
- **Batch Size:** 128

## Project Workflow

1. Load the Sherlock Holmes text dataset.
2. Remove unnecessary metadata.
3. Convert text into lowercase.
4. Clean punctuation and unwanted characters.
5. Split text into sentences.
6. Apply word lemmatization.
7. Convert words into numerical tokens.
8. Generate n-gram sequences.
9. Apply padding to sequences.
10. Split data into training and testing sets.
11. Build the LSTM model.
12. Train and evaluate the model.
13. Predict the next word from user input.

## How to Run the Project

1. Open Google Colab.
2. Create a new notebook.
3. Import the required Python libraries.
4. Upload the Sherlock Holmes dataset.
5. Run the preprocessing steps.
6. Generate training sequences.
7. Build and compile the LSTM model.
8. Train the model using `model.fit()`.
9. Run the prediction function.
10. Enter your own sentence to get the predicted next word.

## Example

**User Input:**

```text
sherlock holmes was
```

**Model Output:**

```text
Predicted Next Word: [Model Prediction]
```

*The actual predicted word depends on the trained model.*

## Prediction Interface

The model allows users to enter sentences interactively.

```python
while True:
    sentence = input("Enter your sentence: ")

    if sentence.lower() == "exit":
        print("Program closed!")
        break

    result = predict_next_word(sentence)

    print("Predicted Next Word:", result)
```

## Limitations

- The model predicts only one next word.
- Predictions depend on the training dataset.
- Unknown words may be ignored.
- Predicted words may appear in their lemmatized form.
- The model does not guarantee grammatically correct predictions.

## Future Improvements

- Train the model on larger datasets.
- Improve prediction accuracy.
- Implement multiple-word prediction.
- Develop a web-based user interface.
- Deploy the model as an API using FastAPI.

## Author

**Shayan Khan**

## Project Type

Natural Language Processing (NLP)  
Deep Learning  
Next Word Prediction

## Dataset Attribution

Training text: *The Adventures of Sherlock Holmes* by Arthur Conan Doyle.

Source: [Project Gutenberg](https://www.gutenberg.org/)

