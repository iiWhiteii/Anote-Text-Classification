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

SEFIT
| Labels    | 20     | 30     | 40     | 50     | 60     | 70     | 80     | 90     | 100    | 110    | 120    | 130    | 140    | 150    |
|-----------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
| Accuracy  | 76.70% | 86.70% | 90.10% | 90.10% | 90.80% | 90.40% | 91.50% | 91.20% | 91.10% | 91.40% | 91.30% | 90.90% | 91.30% | 91.00% |
| Precision | 73.99% | 83.68% | 89.15% | 88.32% | 88.99% | 88.50% | 89.99% | 89.85% | 89.32% | 89.63% | 89.67% | 89.06% | 89.53% | 89.40% |
| Recall    | 81.52% | 88.33% | 87.66% | 88.65% | 89.32% | 89.34% | 90.30% | 90.14% | 89.71% | 90.17% | 90.39% | 89.91% | 90.02% | 89.78% |


BERT
| Labels    | 10     | 20     | 30     | 40     | 50     | 60     | 70     | 80     | 90     | 100    | 110    | 120    | 130    | 140    | 150    |
|-----------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
| Accuracy  | 20.00% | 29.30% | 24.90% | 37.10% | 41.40% | 60.00% | 73.00% | 78.20% | 91.00% | 91.60% | 91.40% | 91.60% | 91.50% | 91.90% | 92.00% |
| Precision | 60.05% | 62.84% | 48.89% | 56.69% | 84.80% | 85.35% | 89.59% | 87.33% | 91.36% | 91.14% | 91.16% | 91.17% | 90.32% | 90.71% | 90.48% |
| Recall    | 19.22% | 19.46% | 23.52% | 28.79% | 30.27% | 50.02% | 60.90% | 68.62% | 88.53% | 90.16% | 89.54% | 90.03% | 89.36% | 89.35% | 89.76% |




# Finance Dataset

 FT-GPT3.5 Turbo
| Labels    | 10      | 20      | 30      | 40      | 50      | 60      | 70      | 80      | 90      | 100     | 110     | 120     | 130     | 140     | 150     |
|-----------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
| Accuracy  | 80.88%  | 86.88%  | 78.25%  | 58.25%  | 93.63%  | 89.50%  | 91.63%  | 81.50%  | 95.75%  | 96.38%  | 92.75%  | 94.13%  | 89.63%  | 95.75%  | 96.50%  |
| Precision | 83.80%  | 87.70%  | 84.14%  | 77.55%  | 92.98%  | 89.60%  | 91.21%  | 84.26%  | 95.41%  | 95.80%  | 91.95%  | 93.21%  | 89.95%  | 94.39%  | 95.93%  |
| Recall    | 68.70%  | 90.40%  | 80.60%  | 56.31%  | 95.52%  | 93.19%  | 94.38%  | 89.53%  | 96.96%  | 97.50%  | 95.53%  | 96.18%  | 93.84%  | 97.35%  | 97.42%  | 


SEFIT
| Labels    | 20      | 30      | 40      | 50      | 60      | 70      | 80      | 90      | 100     | 110     | 120     | 130     | 140     | 150     |
|-----------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
| Accuracy  | 76.70%  | 86.70%  | 90.10%  | 90.10%  | 90.80%  | 90.40%  | 91.50%  | 91.20%  | 91.10%  | 91.40%  | 91.30%  | 90.90%  | 91.30%  | 91.00%  |
| Precision | 73.99%  | 83.68%  | 89.15%  | 88.32%  | 88.99%  | 88.50%  | 89.99%  | 89.85%  | 89.32%  | 89.63%  | 89.67%  | 88.74%  | 89.53%  | 89.40%  |
| Recall    | 81.52%  | 88.33%  | 87.66%  | 88.65%  | 89.32%  | 89.34%  | 90.30%  | 90.14%  | 89.71%  | 90.17%  | 90.39%  | 89.91%  | 90.02%  | 89.78%  |


BERT
| Labels    | 10      | 20      | 30      | 40      | 50      | 60      | 70      | 80      | 90      | 100     | 110     | 120     | 130     | 140     | 150     |
|-----------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
| Accuracy  | 4.37%   | 61.80%  | 85.27%  | 88.14%  | 89.14%  | 88.89%  | 90.14%  | 90.76%  | 92.38%  | 86.64%  | 91.39%  | 92.63%  | 92.13%  | 93.63%  | 93.26%  |
| Precision | 67.01%  | 60.99%  | 70.91%  | 93.58%  | 89.63%  | 87.91%  | 89.99%  | 66.00%  | 91.39%  | 63.78%  | 67.40%  | 68.34%  | 93.47%  | 92.35%  | 92.35%  |
| Recall    | 34.68%  | 33.37%  | 41.67%  | 43.68%  | 48.42%  | 48.97%  | 55.10%  | 62.07%  | 64.02%  | 61.07%  | 59.72%  | 62.40%  | 62.40%  | 48.42%  | 49.23%  |

# Trec Coarse Label Dataset

 FT-GPT3.5 Turbo
| Labels | 10    | 20    | 30    | 40    | 50    | 60    | 70    | 80    | 90    | 100   | 110   | 120   | 130   | 140   | 150   |
|--------|------|------|------|------|------|------|------|------|------|-------|-------|-------|-------|-------|-------|
| Accuracy | 76% | 85.4% | 78.2% | 83% | 92.6% | 89.8% | 90.8% | 92.6% | 94.2% | 93.2% | 94% | 94.6% | 94.8% | 94.2% | 94.6% |
| Precision | 80.5% | 48.4% | 77.5% | 82.5% | 93.4% | 91.4% | 92.1% | 93.5% | 94.9% | 92.1% | 95.2% | 95.4% | 95.1% | 94.5% | 95.8% |
| Recall | 74.8% | 92.3% | 79.6% | 83.1% | 89.7% | 85.6% | 88% | 89.7% | 91.2% | 90.5% | 91% | 91.4% | 91.8% | 91.4% | 82.8% |




Sefit
| Labels   | 20    | 30    | 40    | 50    | 60    | 70    | 80    | 90    | 100   | 110   | 120   | 130   | 140   | 150   |
|---------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|
| Accuracy | 68%   | 81.2% | 86.8% | 87.4% | 91.2% | 83.8% | 89%   | 92.2% | 93.8% | 91.4% | 92%   | 93.8% | 93%   | 93.6% |
| Precision | 61.09% | 70.11% | 83.44% | 84.09% | 90.36% | 80.58% | 88.94% | 91.54% | 89.15% | 87.2% | 87.68% | 89.22% | 88.96% | 89.27% |
| Recall    | 77.5% | 85.71% | 87.91% | 89.72% | 92.91% | 86.64% | 90.49% | 93%   | 94.5% | 89.93% | 93.31% | 94.65% | 93.62% | 94.51% |


BERT
| Labels | 10   | 20   | 30   | 40   | 50   | 60   | 70   | 80   | 90   | 100  | 110  | 120  | 130  | 140  | 150  |
|--------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Accuracy | 22.6% | 26.6% | 16% | 27% | 39.4% | 70.2% | 80.2% | 83.2% | 86.2% | 81% | 85.8% | 90.8% | 86.6% | 91.6% | 89.6% |
| Precision | 87.1% | 75.7% | 71.7% | 78.6% | 74.6% | 81.6% | 86.3% | 86.1% | 84.9% | 77.5% | 82.4% | 93.4% | 90.6% | 91.1% | 92.9% |
| Recall | 16.7% | 23.1% | 18.9% | 27.7% | 36.6% | 58.2% | 66.7% | 70.1% | 82.6% | 69.5% | 73.5% | 78% | 76.4% | 86.1% | 83.1% |







# Trec Fine Label Dataset

 FT-GPT3.5 Turbo
| Labels | 10   | 20   | 30   | 40   | 50   | 60   | 70   | 80   | 90   | 100  | 110  | 120  | 130  | 140  | 150  |
|--------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Accuracy | 67% | 74.2% | 75% | 77% | 79.8% | 81.6% | 82% | 80.6% | 82.6% | 86% | 87% | 85.2% | 86.8% | 86.2% | 88% |
| Precision | 69.4% | 66.9% | 67.6% | 69.1% | 71.1% | 69.1% | 73.9% | 73.9% | 75.5% | 74.2% | 77.2% | 76.8% | 73.9% | 73.9% | 78.45% |
| Recall | 51.8% | 68.6% | 67.6% | 67.1% | 69.8% | 70.3% | 68.3% | 70.07% | 73.72% | 76.47% | 78.32% | 75.17% | 79.55% | 79.93% | 81.13% |



| Label | 20    | 30    | 40    | 50    | 60    | 70    | 80    | 90    | 100   | 110   | 120   | 130   | 140   | 150   |
|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|
| Accuracy  | 37.8% | 50.4% | 55.6% | 55.4% | 61.4% | 61.0% | 64.4% | 66.0% | 69.2% | 70.8% | 70.2% | 73.2% | 73.2% | 74.4% |
| Precision | 14.93% | 18.23% | 21.04% | 25.71% | 32.42% | 36.16% | 37.75% | 39.97% | 45.90% | 45.41% | 42.62% | 48.14% | 47.28% | 49.30% |
| Recall    | 77.68% | 72.65% | 76.09% | 77.19% | 80.86% | 79.70% | 73.84% | 74.70% | 76.84% | 80.40% | 79.31% | 76.81% | 74.52% | 73.55% |








BERT
| Labels | 10   | 20   | 30   | 40   | 50   | 60   | 70   | 80   | 90   | 100  | 110  | 120  | 130  | 140  | 150  |
|--------|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Accuracy | 4.6% | 5.8% | 3.6% | 10.6% | 18.8% | 26.4% | 26.0% | 35.8% | 41.2% | 46.8% | 67.6% | 77.2% | 79.2% | 80.6% | 80.8% |
| Precision | 88.3% | 81.3% | 69.4% | 82.8% | 89.5% | 87.2% | 90.4% | 90.4% | 89.1% | 87.3% | 85.6% | 87.6% | 85.4% | 88.3% | 84.96% |
| Recall | 2.2% | 2.2% | 7.8% | 5.8% | 7.9% | 11.3% | 11.9% | 16.2% | 23.95% | 30.26% | 44.22% | 49.37% | 55.06% | 57.54% | 57.54% |























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
