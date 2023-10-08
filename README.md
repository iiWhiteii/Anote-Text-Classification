# Anote-Text-Classification

We are actively engaged in developing and testing diverse models such as BERT, GPT-4, RNN, and more, with a focus on text classification predictions.

## BERT Model Implementation:
I have successfully implemented and fine-tuned a BERT model to generate predictions on the testing data sourced from the TREC dataset provided by Hugging Face. For instance, when presented with a question like "Who is Galileo?" my model strives to predict that the question pertains to an inquiry about a human. 

![Testing Snapshot 1](https://github.com/Whiteii/Anote-Text-Classification/blob/main/FineLabel/Capture.JPG)

While the BERT model demonstrates an impressive 93% accuracy on the testing data, it's crucial to acknowledge that real-world applications often involve unstructured data, and we may encounter lower accuracy expectations. To tackle this challenge, we employ a technique known as active learning.

![Testing Snapshot 2](https://github.com/Whiteii/Anote-Text-Classification/blob/main/FineLabel/Capture2.JPG)
![Confusion Matrix](https://github.com/Whiteii/Anote-Text-Classification/blob/main/FineLabel/ConfusionMatrix.JPG)






