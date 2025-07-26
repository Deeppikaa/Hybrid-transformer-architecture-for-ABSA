# A hybrid transformer architecture for unsupervised aspect based sentiment analysis

## 🎯 Overview

This project tackles the challenge of understanding customer sentiment in hotel reviews by implementing a two-stage pipeline:
1. **Aspect Extraction** using BERT Topic modeling
2. **Sentiment Analysis** using a novel GPT-2 + BERT fusion model


## 📊 Dataset

We utilized the [515K Hotel Reviews Data in Europe](https://www.kaggle.com/datasets/jiashenliu/515k-hotel-reviews-data-in-europe) from Kaggle, providing a rich foundation for training and evaluation.

## 🔍 Methodology

### Stage 1: Aspect Extraction with BERT Topic

Using BERT Topic modeling, we identified 5 key aspects that customers commonly discuss in hotel reviews:

```
{0: 'Room Cleanliness and Comfort',
 1: 'Booking Experience and Room Issues',
 2: 'Hotel Location and Accessibility',
 3: 'Staff Interaction and Check-in Experience',
 4: 'Breakfast Quality and Dining Service'}
```


**Quality Validation**: We achieved optimal topic coherence and silhouette scores, confirming that 5 aspects provide the best representation of customer concerns.

<img width="1400" height="600" alt="coherence_silhouette_score" src="https://github.com/user-attachments/assets/03c3e6f5-2825-47da-9a35-75b5c169c48f" />

### Stage 2: Sentiment Analysis with GPT-2 + BERT Fusion

Our innovative fusion model combines the strengths of both architectures:
- **GPT-2**: Contextual understanding and text generation capabilities
- **BERT**: Bidirectional encoding for comprehensive sentiment comprehension

<img width="507" height="460" alt="simplified_model_architecture" src="https://github.com/user-attachments/assets/61665ff0-d50d-4eb3-8491-17042917b355" />

## 📈 Results

### Model Performance
Our fusion model demonstrates strong performance across all metrics. Detailed classification reports with precision, recall, and F1-scores are available in: [results_summary.txt](https://github.com/user-attachments/files/21235803/results_summary.txt)

### Training Dynamics
The model showed excellent convergence with stable training and validation loss curves:

<img width="989" height="990" alt="training vs validation loss" src="https://github.com/user-attachments/assets/643b9973-83e7-4c59-bc64-07c7e26316c0" />

## 🛠️ Usage

### 1. Aspect Extraction
Run the `paper-2-aspect-extract-kaggle-code.ipynb` notebook to extract aspects from hotel reviews:

<img width="1213" height="621" alt="Screenshot 2025-07-15 at 7 21 44 PM 1" src="https://github.com/user-attachments/assets/eb9998e8-1d20-413f-a50e-15949e417071" />

### 2. Model Training & Inference
Execute the model training notebook `multimodal-fusion-gpt2-bert-0-2-epoch-source-code.ipynb` to fine-tune the GPT-2 + BERT fusion model:

<img width="1187" height="491" alt="Screenshot 2025-07-15 at 8 09 06 PM" src="https://github.com/user-attachments/assets/409895ca-1927-4d8b-b41f-a30a9c433de6" />

## 📁 Repository Structure

```
├── paper-2-aspect-extract-kaggle-code.ipynb                      # BERT Topic modeling for aspect extraction
├── multimodal-fusion-gpt2-bert-0-2-epoch-source-code.ipynb       # GPT-2 + BERT fusion model training
├── results_summary.txt                                           # Detailed performance metrics
└── README.md                                                     # This file
```

## 🔬 Technical Contributions

- **Novel Fusion Architecture**: First implementation of GPT-2 + BERT fusion for aspect-based sentiment analysis
- **Comprehensive Aspect Discovery**: Systematic identification of 5 key hotel review aspects
- **Robust Evaluation**: Multi-metric validation ensuring model reliability

## 🎓 Research Impact

This work advances the state-of-the-art in aspect-based sentiment analysis by demonstrating how modern transformer architectures can be effectively combined for nuanced understanding of customer feedback.

---

*For detailed implementation and results, please refer to the provided Jupyter notebooks and result files.*


