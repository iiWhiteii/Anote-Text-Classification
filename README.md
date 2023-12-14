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
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/Amazon%20Dataset/Overall%20Evaluation/Model%20Performance.png" width="700">
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/Banking%20Dataset/Overall%20Evaluation/output.png" width="700">
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/Craigslist%20Dataset/Overall%20Evaluation/output.png" width="700">
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/Finance%20Dataset/Overall%20Evaluation/output.png" width="700">
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/TREC%20Dataset/Coarse_Label/Overall%20Evaluation/output.png" width="700">
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/TREC%20Dataset/Fine_Label/Overall%20Evaluation/output.png" width="700">

  




  

</p>

Banking dataset comprises 77 distinct labels, each denoting a specific inquiry or transaction within the realm of banking. This dataset contains 2000 rows of data. Notably, even with a reduced set of 150 labels, the model continues to exhibit strong performance.


We observed the initial effectiveness of GPT-3.5 Turbo's predictions, demonstrating notable accuracy even without fine-tuning based on feedback, likely due to its pretraining on general knowledge. As we incrementally provided and fine-tuned with 10 labels, extending to 150, we compared its performance against all other implemented models, and GPT-3.5 emerged as the top performer. This highlights that relying solely on a general AI like GPT-3.5 for labeling is not effient.




## Model Performance Comparison

# Amazon Dataset

# FT-GPT3.5 Turbo
| Label          | 10      | 20      | 30      | 40      | 50      | 60      | 70      | 80      | 90      | 100     | 110     | 120     | 130     | 140     | 150     |
|------------------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
| Accuracy         | 53.75%  | 49.00%  | 52.75%  | 55.75%  | 65.00%  | 61.00%  | 61.25%  | 57.50%  | 64.75%  | 71.00%  | 66.25%  | 64.50%  | 57.00%  | 58.50%  | 63.75%  |
| Precision        | 41.06%  | 49.68%  | 42.62%  | 42.89%  | 68.61%  | 67.66%  | 69.76%  | 68.56%  | 64.03%  | 67.15%  | 63.99%  | 69.02%  | 69.10%  | 68.36%  | 72.56%  |
| Recall           | 35.02%  | 38.23%  | 49.35%  | 37.71%  | 52.22%  | 46.12%  | 45.52%  | 43.13%  | 47.04%  | 53.23%  | 47.70%  | 54.97%  | 40.32%  | 44.65%  | 48.53%  | 

# SEFIT 

| Label   | 20      | 30      | 40      | 50      | 60      | 70      | 80      | 90      | 100     | 110     | 120     | 130     | 140     | 150     |
|-----------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
| Accuracy  | 58.25%  | 62.55%  | 62.95%  | 67.55%  | 67.55%  | 67.05%  | 68.45%  | 67.50%  | 69.20%  | 69.40%  | 68.45%  | 69.95%  | 68.30%  | 66.95%  |
| Precision | 49.33%  | 49.84%  | 49.45%  | 52.10%  | 52.42%  | 54.89%  | 51.99%  | 51.10%  | 54.14%  | 53.43%  | 53.91%  | 54.57%  | 51.86%  | 54.30%  |
| Recall    | 45.47%  | 51.26%  | 51.15%  | 53.44%  | 53.65%  | 56.33%  | 53.37%  | 53.20%  | 54.92%  | 56.72%  | 56.46%  | 57.42%  | 55.88%  | 57.28%  |

# BERT

| Labels   | 10       | 20       | 30       | 40       | 50       | 60       | 70       | 80       | 90       | 100      | 110      | 120      | 130      | 140      | 150      |
|-----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|
| Accuracy  | 10.05%   | 10.10%   | 10.05%   | 18.25%   | 51.85%   | 53.45%   | 49.30%   | 56.85%   | 50.95%   | 61.30%   | 62.35%   | 63.45%   | 63.80%   | 62.20%   | 60.75%   |
| Precision | 64.23%   | 66.01%   | 67.00%   | 56.01%   | 70.86%   | 73.71%   | 71.44%   | 77.04%   | 76.16%   | 41.99%   | 60.72%   | 49.02%   | 49.97%   | 51.90%   | 57.52%   |
| Recall    | 20.17%   | 20.27%   | 20.09%   | 23.75%   | 24.85%   | 25.61%   | 25.13%   | 28.90%   | 24.28%   | 35.63%   | 38.23%   | 46.11%   | 44.40%   | 44.04%   | 48.02%   |















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
