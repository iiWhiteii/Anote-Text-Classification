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










# Banking Dataset

 FT-GPT3.5 Turbo
| Labels   | 10       | 20       | 30       | 40       | 50       | 60       | 70       | 80       | 90       | 100      | 110      | 120      | 130      | 140      | 150      |
|-----------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
| Accuracy  | 61.00%  | 71.00%  | 75.00%  | 79.00%  | 83.00%  | 72.30%  | 74.00%  | 74.00%  | 76.20%  | 76.60%  | 76.90%  | 75.80%  | 76.80%  | 76.80%  | 77.20%  |
| Precision | 71.37%  | 76.97%  | 79.68%  | 88.08%  | 87.10%  | 71.02%  | 76.95%  | 75.29%  | 78.84%  | 74.66%  | 76.82%  | 75.00%  | 72.85%  | 77.06%  | 73.58%  |
| Recall    | 63.56%  | 71.11%  | 77.44%  | 79.02%  | 81.75%  | 75.03%  | 74.56%  | 75.04%  | 76.71%  | 77.98%  | 77.43%  | 77.21%  | 79.04%  | 78.17%  | 79.27%  |


SEFIT
| Label    | 30                  | 40                  | 50                  | 60                  | 70                  | 80                  | 90                  | 100                 | 110                 | 120                 | 130                 | 140                 | 150                 |
|----------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|---------------------|
| Accuracy | 18.97%              | 23.32%              | 26.18%              | 30.18%              | 32.93%              | 37.54%              | 42.59%              | 45.15%              | 47.30%              | 49.60%              | 53.10%              | 52.00%              | 54.30%              |
| Precision| 19.84%              | 24.12%              | 26.91%              | 31.33%              | 34.27%              | 38.92%              | 44.05%              | 46.30%              | 48.69%              | 50.58%              | 54.50%              | 53.38%              | 55.68%              |
| Recall   | 80.62%              | 78.83%              | 75.29%              | 74.88%              | 71.22%              | 68.12%              | 69.70%              | 66.87%              | 67.66%              | 65.87%              | 65.72%              | 67.19%              | 66.78%              |


 BERT 
| Labels   | 10       | 20       | 30       | 40       | 50       | 60       | 70       | 80       | 90       | 100      | 110      | 120      | 130      | 140      | 150      |
|-----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|----------|
| Accuracy  | 1.65%    | 1.70%    | 2.05%    | 1.80%    | 1.65%    | 2.75%    | 3.45%    | 4.10%    | 5.36%    | 7.76%    | 9.11%    | 14.36%   | 18.72%   | 19.37%   | 23.77%   |
| Precision | 83.26%   | 82.44%   | 80.66%   | 71.72%   | 77.51%   | 76.99%   | 83.80%   | 85.27%   | 84.72%   | 84.66%   | 83.62%   | 80.24%   | 74.28%   | 72.58%   | 70.64%   |
| Recall    | 1.53%    | 1.55%    | 1.98%    | 1.75%    | 1.67%    | 2.78%    | 3.46%    | 4.11%    | 5.32%    | 7.60%    | 8.90%    | 14.14%   | 18.42%   | 19.25%   | 23.65%   |



# Craigslist Dataset



 FT-GPT3.5 Turbo
| Labels    | 10     | 20     | 30     | 40     | 50     | 60     | 70     | 80     | 90     | 100    | 110    | 120    | 130    | 140    | 150    |
|-----------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
| Accuracy  | 88.20% | 94.10% | 93.20% | 94.20% | 88.90% | 91.10% | 92.80% | 94.90% | 94.00% | 94.80% | 95.10% | 95.30% | 95.30% | 94.70% | 95.70% |
| Precision | 90.46% | 70.08% | 92.44% | 92.67% | 91.28% | 79.15% | 79.26% | 94.06% | 93.36% | 94.01% | 94.09% | 80.94% | 93.64% | 93.61% | 94.68% |
| Recall    | 80.34% | 93.82% | 89.36% | 91.79% | 80.96% | 87.11% | 90.23% | 92.53% | 91.29% | 92.25% | 93.06% | 94.35% | 93.62% | 92.90% | 93.79% |

BERT
| Labels    | 10     | 20     | 30     | 40     | 50     | 60     | 70     | 80     | 90     | 100    | 110    | 120    | 130    | 140    | 150    |
|-----------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
| Accuracy  | 20.00% | 29.30% | 24.90% | 37.10% | 41.40% | 60.00% | 73.00% | 78.20% | 91.00% | 91.60% | 91.40% | 91.60% | 91.50% | 91.90% | 92.00% |
| Precision | 60.05% | 62.84% | 48.89% | 56.69% | 84.80% | 85.35% | 89.59% | 87.33% | 91.36% | 91.14% | 91.16% | 91.17% | 90.32% | 90.71% | 90.48% |
| Recall    | 19.22% | 19.46% | 23.52% | 28.79% | 30.27% | 50.02% | 60.90% | 68.62% | 88.53% | 90.16% | 89.54% | 90.03% | 89.36% | 89.35% | 89.76% |

SEFIT
| Labels    | 20     | 30     | 40     | 50     | 60     | 70     | 80     | 90     | 100    | 110    | 120    | 130    | 140    | 150    |
|-----------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
| Accuracy  | 76.70% | 86.70% | 90.10% | 90.10% | 90.80% | 90.40% | 91.50% | 91.20% | 91.10% | 91.40% | 91.30% | 90.90% | 91.30% | 91.00% |
| Precision | 73.99% | 83.68% | 89.15% | 88.32% | 88.99% | 88.50% | 89.99% | 89.85% | 89.32% | 89.63% | 89.67% | 89.06% | 89.53% | 89.40% |
| Recall    | 81.52% | 88.33% | 87.66% | 88.65% | 89.32% | 89.34% | 90.30% | 90.14% | 89.71% | 90.17% | 90.39% | 89.91% | 90.02% | 89.78% |


















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
