# Sentiment Analysis with BERT on Twitter Data

This project demonstrates a complete end-to-end workflow for sentiment analysis using a BERT model. It covers data preprocessing, model training, and evaluation on a Twitter dataset, showcasing how to fine-tune BERT for classifying text sentiments as positive, negative, or neutral.

## Project Structure

### 1. **Data Preprocessing**
  - Loads the *Twitter Entity Sentiment Analysis* dataset from Kaggle.
  - Cleans the dataset by removing irrelevant entries based on the dataset description.
  - Converts sentiment labels into numerical values: positive (`1`), negative (`0`), and neutral (`2`).
  - Tokenizes the text using the `bert-base-uncased` tokenizer.
  - Converts the processed data into a Hugging Face dataset format and saves it locally.

### 2. **Model Training**
  - Fine-tunes a pretrained BERT model using `BertForSequenceClassification`.
  - Uses a data collator function for dynamic padding to ensure efficient batch processing.
  - Trains the model on the preprocessed dataset, optimizing for sentiment classification.

### 3. **Model Evaluation**
  - Evaluates the fine-tuned model on a test set to measure accuracy.
  - Compares the performance of the fine-tuned model against the non-fine-tuned (pretrained) version.
  - Demonstrates the model's prediction capabilities on three custom sentences to verify correct sentiment classification.

## Conclusion

The evaluation confirms that fine-tuning the BERT model for sentiment analysis leads to a substantial performance boost. Both the test set results and custom sentence predictions demonstrate that the model is well-equipped to accurately classify the sentiment of a given text.

### Examples

**Sentence 1**: I am so excited about this new project\
**Predicted sentiment**: positive

**Sentence 2**: Maybe I'll pass by later this week, I don't know yet\
**Predicted sentiment**: neutral

**Sentence**: There's no way I am going there tonight\
**Predicted sentiment**: negative

