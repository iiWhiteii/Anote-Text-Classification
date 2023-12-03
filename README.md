# Enhancing Language Model Accuracy: The Power of a Few Labeled Examples
<a href="https://medium.com/@Liang./enhancing-language-model-accuracy-the-power-of-a-few-labeled-examples-92eae5771323">
  <img src="https://static.wikia.nocookie.net/logopedia/images/6/63/Colab_favicon_256px.png/revision/latest/scale-to-width-down/170?cb=20201019224542" alt="Medium Icon" width="32px" style="margin-right: 15px;">
  <img src="https://cdn-icons-png.flaticon.com/512/5968/5968906.png" alt="Medium Icon" width="32px">
</a>


**Description:**
As student this project with Anote AI, addressing challenges in Large Language Models (LLMs) like GPT-3.5 Turbo, BERT, and RNN. In the early days, LLMs required extensive labeled data, posing time and cost challenges. Real-world data complexities, being messy and unstructured, made effective analysis difficult.

To overcome these hurdles, we introduce an active learning approach, enhancing text classification accuracy. Similar to providing students with clear examples for better understanding, the strategy involves fine-tuning models through human feedback or providing more label examples.



## Table of Contents

1. [Installation](#installation)
---

### Accuracy Improvement
After fine-tuning the models with human feedback and additional labeled examples, we observed a consistent improvement in accuracy across different datasets. This result supports the effectiveness of the active learning approach in enhancing the models' understanding of specific domains.

### Finding
After fine-tuning the models with human feedback and additional labeled examples, we observed a consistent improvement in accuracy across different datasets. Notably, our experiments revealed that incorporating targeted training on areas where the model is weak played a pivotal role. This iterative approach allowed the model to gradually enhance its proficiency in handling specific domains.

### Benchmark
<p align="center">
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/Banking%20Dataset/Overall%20Evaluation/OverallEvaluation_Banking.JPG" width="700">
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/Craigslist%20Dataset/Overall%20Evaluation/model_performance.JPG" width="700">
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/TREC%20Dataset/Coarse_Label/Overall%20Evaluation/Model%20Performance.JPG" width="700">
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/TREC%20Dataset/Fine_Label/Overall%20Evaluation/Model%20Comparison.JPG" width="700">
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/Finance%20Dataset/Overall%20Evaluation/Capture.JPG" width="700">
  

</p>

Banking dataset comprises 77 distinct labels, each denoting a specific inquiry or transaction within the realm of banking. This dataset contains 2000 rows of data. Notably, even with a reduced set of 150 labels, the model continues to exhibit strong performance.


We observed the initial effectiveness of GPT-3.5 Turbo's predictions, demonstrating notable accuracy even without fine-tuning based on feedback, likely due to its pretraining on general knowledge. As we incrementally provided and fine-tuned with 10 labels, extending to 150, we compared its performance against all other implemented models, and GPT-3.5 emerged as the top performer. This highlights that relying solely on a general AI like GPT-3.5 for labeling is not effient.






#### Model Performance Post-Feedback Comparison:

| Model  | Dataset    | Accuracy | Precision | Recall |
|--------|------------|----------|-----------|--------|
| GPT3.5 | Banking    | 77.00%   | 73.58%    | 79.26% |
| GPT3.5 | Craigslist | 96.00%   | 94.68%    | 93.79% |
| GPT3.5 | TREC       | 95.00%   | 95.81%    | 82.81% |
| BERT   | Banking    | 23.77%   | 70.64%    | 23.64% |
| BERT   | Craigslist | 92.00%   | 90.48%    | 89.56% |
| BERT   | TREC       | 89.60%   | 92.94%    | 83.11% |
| RNN    | Banking    | 18.56%   | 32.79%    | 18.54% |
| RNN    | Craigslist | 34.00%   | 31.10%    | 29.83% |
| RNN    | TREC       | 79.20%   | 73.06%    | 79.35% |




### Confusion Matrix

For a detailed view of the confusion matrix, navigate to the [Overall Evaluation/cm](https://github.com/Whiteii/Anote-Text-Classification/tree/main/Banking%20Dataset/Overall%20Evaluation/CM) for Banking.

For Craigslist, navigate to the [Overall Evaluation/cm](https://github.com/Whiteii/Anote-Text-Classification/tree/main/Craigslist%20Dataset/Overall%20Evaluation/CM).

For TREC, navigate to the [Overall Evaluation/cm](https://github.com/Whiteii/Anote-Text-Classification/tree/main/TREC%20Dataset/Coarse_Label/Overall%20Evaluation/CM).






## Installation

### Prerequisites

Make sure you have Python, pip, and git installed.

### Clone the Repository and Install Dependencies

```bash
git clone https://github.com/Whiteii/Anote-Text-Classification.git
cd Anote-Text-Classification
pip install -r requirements.txt
