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

 FT-GPT3.5 Turbo
| Label          | 10      | 20      | 30      | 40      | 50      | 60      | 70      | 80      | 90      | 100     | 110     | 120     | 130     | 140     | 150     |
|------------------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
| Accuracy         | 53.75%  | 49.00%  | 52.75%  | 55.75%  | 65.00%  | 61.00%  | 61.25%  | 57.50%  | 64.75%  | 71.00%  | 66.25%  | 64.50%  | 57.00%  | 58.50%  | 63.75%  |
| Precision        | 41.06%  | 49.68%  | 42.62%  | 42.89%  | 68.61%  | 67.66%  | 69.76%  | 68.56%  | 64.03%  | 67.15%  | 63.99%  | 69.02%  | 69.10%  | 68.36%  | 72.56%  |
| Recall           | 35.02%  | 38.23%  | 49.35%  | 37.71%  | 52.22%  | 46.12%  | 45.52%  | 43.13%  | 47.04%  | 53.23%  | 47.70%  | 54.97%  | 40.32%  | 44.65%  | 48.53%  | 

SEFIT 
| Label   | 20      | 30      | 40      | 50      | 60      | 70      | 80      | 90      | 100     | 110     | 120     | 130     | 140     | 150     |
|-----------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
| Accuracy  | 58.25%  | 62.55%  | 62.95%  | 67.55%  | 67.55%  | 67.05%  | 68.45%  | 67.50%  | 69.20%  | 69.40%  | 68.45%  | 69.95%  | 68.30%  | 66.95%  |
| Precision | 49.33%  | 49.84%  | 49.45%  | 52.10%  | 52.42%  | 54.89%  | 51.99%  | 51.10%  | 54.14%  | 53.43%  | 53.91%  | 54.57%  | 51.86%  | 54.30%  |
| Recall    | 45.47%  | 51.26%  | 51.15%  | 53.44%  | 53.65%  | 56.33%  | 53.37%  | 53.20%  | 54.92%  | 56.72%  | 56.46%  | 57.42%  | 55.88%  | 57.28%  |

 BERT
| Labels   | 10       | 20       | 30       | 40       | 50       | 60       | 70       | 80       | 90       | 100      | 110      | 120      | 130      | 140      | 150      |
|-----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|
| Accuracy  | 10.05%   | 10.10%   | 10.05%   | 18.25%   | 51.85%   | 53.45%   | 49.30%   | 56.85%   | 50.95%   | 61.30%   | 62.35%   | 63.45%   | 63.80%   | 62.20%   | 60.75%   |
| Precision | 64.23%   | 66.01%   | 67.00%   | 56.01%   | 70.86%   | 73.71%   | 71.44%   | 77.04%   | 76.16%   | 41.99%   | 60.72%   | 49.02%   | 49.97%   | 51.90%   | 57.52%   |
| Recall    | 20.17%   | 20.27%   | 20.09%   | 23.75%   | 24.85%   | 25.61%   | 25.13%   | 28.90%   | 24.28%   | 35.63%   | 38.23%   | 46.11%   | 44.40%   | 44.04%   | 48.02%   |


SEFIT
| Label    | 30                  | 40                  | 50                  | 60                  | 70                  | 80                  | 90                  | 100                 | 110                 | 120                 | 130                 | 140                 | 150                 |
|----------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|
| Accuracy | 0.1896896896896897  | 0.23323323323323322 | 0.26176176176176175 | 0.30180180180180183 | 0.32932932932932935 | 0.37537537537537535 | 0.42592592592592593 | 0.45145145145145144 | 0.47297297297297297 | 0.495995995995996   | 0.531031031031031   | 0.52002002002002    | 0.5430430430430431  |
| Precision| 0.19840352539110304 | 0.24115502123407265 | 0.2690534959112034  | 0.3133128292117902  | 0.3427033778061784  | 0.3891507531298948  | 0.4405313156722791  | 0.4630165681689681  | 0.48692605368849773 | 0.5058265685724308  | 0.5450124252649049  | 0.533842149565976   | 0.5568390616498005  |
| Recall   | 0.8062029212513475  | 0.7883122235531191  | 0.7529234847151665  | 0.7488341087026137  | 0.7122209244050073  | 0.6811518182547538  | 0.6970445478042987  | 0.6686823234052207  | 0.6766224162821346  | 0.6587283518082925  | 0.6572342338278107  | 0.6718631316723803  | 0.6678281291645879  |





#Banking

 FT-GPT3.5 Turbo
| Labels   | 10       | 20       | 30       | 40       | 50       | 60       | 70       | 80       | 90       | 100      | 110      | 120      | 130      | 140      | 150      |
|-----------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
| Accuracy  | 61.00%  | 71.00%  | 75.00%  | 79.00%  | 83.00%  | 72.30%  | 74.00%  | 74.00%  | 76.20%  | 76.60%  | 76.90%  | 75.80%  | 76.80%  | 76.80%  | 77.20%  |
| Precision | 71.37%  | 76.97%  | 79.68%  | 88.08%  | 87.10%  | 71.02%  | 76.95%  | 75.29%  | 78.84%  | 74.66%  | 76.82%  | 75.00%  | 72.85%  | 77.06%  | 73.58%  |
| Recall    | 63.56%  | 71.11%  | 77.44%  | 79.02%  | 81.75%  | 75.03%  | 74.56%  | 75.04%  | 76.71%  | 77.98%  | 77.43%  | 77.21%  | 79.04%  | 78.17%  | 79.27%  |







 BERT 
| Labels   | 10       | 20       | 30       | 40       | 50       | 60       | 70       | 80       | 90       | 100      | 110      | 120      | 130      | 140      | 150      |
|-----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|
| Accuracy  | 1.65%    | 1.70%    | 2.05%    | 1.80%    | 1.65%    | 2.75%    | 3.45%    | 4.10%    | 5.36%    | 7.76%    | 9.11%    | 14.36%   | 18.72%   | 19.37%   | 23.77%   |
| Precision | 83.26%   | 82.44%   | 80.66%   | 71.72%   | 77.51%   | 76.99%   | 83.80%   | 85.27%   | 84.72%   | 84.66%   | 83.62%   | 80.24%   | 74.28%   | 72.58%   | 70.64%   |
| Recall    | 1.53%    | 1.55%    | 1.98%    | 1.75%    | 1.67%    | 2.78%    | 3.46%    | 4.11%    | 5.32%    | 7.60%    | 8.90%    | 14.14%   | 18.42%   | 19.25%   | 23.65%   |
















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
