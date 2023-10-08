# Anote-Text-Classification

We are actively engaged in developing and testing diverse models such as BERT, GPT-4, RNN, and more, with a focus on text classification predictions.

## BERT Model Implementation:
I have successfully implemented and fine-tuned a BERT model to generate predictions on the testing data sourced from the TREC dataset provided by Hugging Face. For instance, when presented with a question like "Who is Galileo?" my model strives to predict that the question pertains to an inquiry about a human. 

![Testing Snapshot 1](https://github.com/Whiteii/Anote-Text-Classification/blob/main/FineLabel/Capture.JPG)

While the BERT model demonstrates an impressive 93% accuracy on the testing data, it's crucial to acknowledge that real-world applications often involve unstructured data, and we may encounter lower accuracy expectations. To tackle this challenge, we employ a technique known as active learning.

## BERT Model Accuracy
![Testing Snapshot 2](https://github.com/Whiteii/Anote-Text-Classification/blob/main/FineLabel/Capture2.JPG)     


## Confusion Matrix 
<img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/FineLabel/ConfusionMatrix.JPG" alt="Confusion Matrix" width="600">


## Active Learning 
Active learning is a machine learning approach where a model engages with a human annotator to strategically select which instances to label. 
This iterative process helps the model learn more effectively with minimal labeled data, making it particularly useful in situations where obtaining labeled data is challenging or expensive


