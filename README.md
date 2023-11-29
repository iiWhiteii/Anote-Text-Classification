# Enhancing Language Model Accuracy: The Power of a Few Labeled Examples

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

<div style="display: flex; justify-content: space-between;">

  <div style="text-align: left;">

### 1. GPT-3.5 Turbo Fine-Tuned Predictions
![GPT-3.5 Turbo](https://github.com/Whiteii/Anote-Text-Classification/blob/main/Banking%20Dataset/GPT3.5_Turbo/Evaluation/Confusion%20Matrix%20for%20Banking%20GPT3.5_Turbo%20Prediction.png)

  </div>

  <div style="text-align: center;">

### 2. BERT Predictions
![BERT](https://github.com/Whiteii/Anote-Text-Classification/blob/main/Banking%20Dataset/BERT/Evaluation/Confusion%20Matrix%20for%20Banking%20BERT%20Prediction.png)

  </div>

  <div style="text-align: right;">

### 3. RNN Predictions
![RNN](https://github.com/Whiteii/Anote-Text-Classification/blob/main/Banking%20Dataset/RNN/evaluation/Confusion_Matrix_Banking_Label_RNN.JPG)

  </div>

</div>









### Conclusion

The experimental results strongly support our hypothesis. The active learning approach, complemented by fine-tuning capabilities, demonstrated remarkable effectiveness in overcoming challenges associated with LLMs, ultimately leading to improved accuracy and domain-specific proficiency.



















## Installation

### Prerequisites

Make sure you have Python, pip, and git installed.

### Clone the Repository and Install Dependencies

```bash
git clone https://github.com/Whiteii/Anote-Text-Classification.git
cd Anote-Text-Classification
pip install -r requirements.txt

Findings

#### 1. Accuracy Improvement

After fine-tuning the models with human feedback and additional labeled examples, we observed a consistent improvement in accuracy across different datasets. This result supports the effectiveness of the active learning approach in enhancing the models' understanding of specific domains.

#### 2. Domain-Specific Challenges

Our experiments revealed that the active learning approach played a crucial role in addressing domain-specific challenges. The models exhibited increased proficiency in handling intricacies associated with complicated categories in text classification.

#### 3. Adaptability with Fine-Tuning

The recent introduction of fine-tuning capabilities for GPT-3.5 Turbo provided a significant advantage. It allowed us to tailor the models to specific use cases, showcasing the adaptability and customization potential of our approach.

### Conclusion

The experimental results strongly support our hypothesis. The active learning approach, complemented by fine-tuning capabilities, demonstrated remarkable effectiveness in overcoming challenges associated with LLMs, ultimately leading to improved accuracy and domain-specific proficiency.


