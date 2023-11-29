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

### Benchmark On Banking
<p align="center">
  <img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/Banking%20Dataset/Overall%20Evaluation/OverallEvaluation_Banking.JPG" width="700">
</p>

The dataset consists of a total of 77 unique labels, each representing a specific banking-related query or concern. This diverse set of labels reflects a wide range of potential issues and inquiries within the banking domain, providing a comprehensive foundation for analysis and classification tasks.

#### Model Performance Comparison:
- **GPT3.5 Turbo Model:**
  - Accuracy: 61% to 77%
  - Recall: 63.56% to 79.27%
  - Precision: 71.36% to 73.58%

- **BERT Model:**
  - Accuracy: 1% to 23%
  - Recall: 1% to 23.77%
  - Precision: 83% to 70%  <!-- Place BERT in the middle -->

- **RNN Model:**
  - Accuracy: 1% to 18%
  - Recall: 3% to 18%
  - Precision: 87% to 32%  <!-- Place RNN on the left -->


### Benchmark On Craigslist Dataset

#### Model Performance Comparison:
- **GPT3.5 Turbo Model:**
  - Accuracy: 88.2% to 95.7%
  - Recall: 80.34% to 93.79%
  - Precision: 90.46% to 94.68%

- **BERT Model:**
  - Accuracy: 22.6% to 89.6%
  - Recall: 16.66% to 83.11%
  - Precision: 87% to 92%

- **RNN Model:**
  - Accuracy: 1% to 18%
  - Recall: 3% to 18%
  - Precision: 87% to 32%

 <style> table { font-family: "Arial"; } </style> <table> <tr> <th></th> <th>Banking</th> <th>Craigslist</th> <th>TREC</th> </tr> <tr> <td>Accuracy</td> <td>GPT3.5 - 77%</td> <td>GPT3.5 - 96% </td> <td>GPT3.5 - 95%</td> </tr> <tr> <td>Accuracy</td> <td>BERT - 23.77%</td> <td>BERT - 92.00%</td> <td>BERT - 89.60%</td> </tr> <tr> <td>Accuracy</td> <td>RNN - 18.56%</td> <td>RNN - 34.00%</td> <td>RNN - 79.20%</td> </tr> <tr> <td>Precision</td> <td>GPT3.5 - 73.58%</td> <td>GPT3.5 - 94.68%</td> <td>GPT3.5 - 95.81%</td> </tr> <tr> <td>Precision</td> <td>BERT - 70.64%</td> <td>BERT - 90.48%</td> <td>BERT - 92.94%</td> </tr> <tr> <td>Precision</td> <td>RNN - 32.79%</td> <td>RNN - 31.10%</td> <td>RNN - 73.06%</td> </tr> <tr> <td>Recall</td> <td>GPT3.5 - 79.26%</td> <td>GPT3.5 - 93.79%</td> <td>GPT3.5 - 82.81%</td> </tr> <tr> <td>Recall</td> <td>BERT - 23.64%</td> <td>BERT - 89.56%</td> <td>BERT - 83.11%</td> </tr> <tr> <td>Recall</td> <td>RNN - 18.54%</td> <td>RNN - 29.83%</td> <td>RNN - 79.35%</td> </tr> </table>








### Confusion Matrix
<img src="https://github.com/Whiteii/Anote-Text-Classification/blob/main/Banking%20Dataset/GPT3.5_Turbo/Evaluation/Confusion%20Matrix%20for%20Banking%20GPT3.5_Turbo%20Prediction.png" width="500">



## Installation

### Prerequisites

Make sure you have Python, pip, and git installed.

### Clone the Repository and Install Dependencies

```bash
git clone https://github.com/Whiteii/Anote-Text-Classification.git
cd Anote-Text-Classification
pip install -r requirements.txt
