# Fair_Frame-Media-Bias-Detection-and-Mitigation
This project focuses on identifying and reducing bias in media articles. It involves two main tasks:

### 1. Bias Detection – Predicting the degree of bias in a given piece of text.

### 2. Bias Mitigation – Rephrasing biased sentences to make them more neutral and objective.

This project proposes a ML based approach to systematically detect and reduce bias in textual content, ensuring that news articles remain as neutral and objective as possible. By leveraging the power of transformer-based architectures, the system can analyze textual patterns, detect bias, and generate mitigated content with minimal human intervention. The bias detection model assigns a bias score to each piece of text, indicating the degree of bias present in the content. This score serves as a crucial metric for assessing the effectiveness of bias mitigation techniques.
## 📌 Methodology
The process begins with the BABE dataset, where a bias score function assigns numerical bias scores to each entry, creating an updated dataset. For bias detection, input text is processed through a pre-trained BERT model, which predicts its bias score. If the predicted score is greater than 3, the text is flagged as biased and requires mitigation. If the score is less than 3, the text is considered unbiased and is directly accepted as output.
When a text is identified as biased, it is passed to the T5 model, which attempts to rephrase it in a more neutral form. The mitigated text is subsequently re-evaluated by the BERT model to verify its bias score. This iterative process continues until the text is classified as unbiased, ensuring effective bias reduction while maintaining the integrity of the original content.
## 🧰 Technologies Used
Python

PyTorch

Transformers (HuggingFace)

Scikit-learn

ROUGE, BLEU

BERT, T5

## 📈 Model Architecture
### Bias Detection:
Model: BERT (base-uncased)

Task: Sequence regression (predicting bias score)

### Bias Mitigation:
Model: T5-large

Task: Text-to-text generation (rephrasing to reduce bias)
