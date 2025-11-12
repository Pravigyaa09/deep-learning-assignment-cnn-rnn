Deep Learning Assignment: CNN & LSTM using TensorFlow/Keras

Name: Pravigya Acharya  
USN: 1RF22IS059  
Course: Deep Learning Laboratory  
Institute: RV Institute of Technology and Management  
Date: 11 November 2025  

---

Assignment Overview

This assignment involves designing and implementing **two deep learning models** using **Python and TensorFlow/Keras**:

1. Convolutional Neural Network (CNN)– for Image Classification  
2. Recurrent Neural Network (RNN) using LSTM units– for Sentiment Analysis  

Both models were trained, evaluated, and documented in Google Colab, and the implementation files have been uploaded to this GitHub repository along with the PDF reports.

---

1. Convolutional Neural Network (CNN)
Task :Image Classification using the CIFAR-10 dataset  
Dataset details:
- CIFAR-10 dataset contains **60,000 color images (32x32)** divided into 10 classes.
- 50,000 images used for training and 10,000 for testing.

Architecture Highlights:
- Data Augmentation (Random Flip, Rotation, Zoom)  
- 3 Convolutional Blocks (Conv2D + BatchNorm + MaxPooling)  
- Dense Layers with Dropout regularization  
- Adam Optimizer + EarlyStopping + ReduceLROnPlateau  

Performance:
| Metric                | Value  |
|:-------               |:------:|
| Training Accuracy     | ~80%   |
| Validation Accuracy   | ~81%   |
| Test Accuracy         | 0.8052 |

Classification Report (Test Set):
| Class      | Precision | Recall | F1-score |
|:------     |:----------|:-------|:---------|
| airplane   | 0.79      | 0.86   | 0.82     |
| automobile | 0.88      | 0.92   | 0.90     |
| bird       | 0.82      | 0.68   | 0.74     |
| cat        | 0.68      | 0.59   | 0.63     |
| deer       | 0.78      | 0.75   | 0.77     |
| dog        | 0.78      | 0.69   | 0.73     |
| frog       | 0.77      | 0.92   | 0.84     |
| horse      | 0.80      | 0.88   | 0.84     |
| ship       | 0.92      | 0.86   | 0.89     |
| truck      | 0.82      | 0.90   | 0.86     |
Overall Accuracy:81% 

Model File:`cnn_image_classification.ipynb`  
Saved Model:`cnn_model.keras`  
PDF Report: `reports/cnn_image_classification.pdf`

---

2. Recurrent Neural Network (RNN – LSTM)
Task: Sentiment Analysis using IMDb Reviews dataset  
Dataset details:
- IMDb dataset with **50,000 labeled reviews** (25,000 training + 25,000 testing)
- Labels: 0 = Negative, 1 = Positive

Architecture Highlights:
- Embedding layer with 20,000 words  
- Bidirectional LSTM (128 units)  
- Dropout & SpatialDropout for regularization  
- Dense layers for sentiment prediction  
- Adam Optimizer + EarlyStopping + ReduceLROnPlateau  

Performance:
| Metric              | Value  |
|:-------------------:|:------:|
| Training Accuracy   | ~97%   |
| Validation Accuracy | ~87%   |
| Test Accuracy       | 0.8561 |

Classification Report (Test Set):
| Label    | Precision  | Recall  | F1-score  |
|:------   |:----------:|:-------:|:---------:|
| Negative | 0.82       | 0.91    | 0.86      |
| Positive | 0.90       | 0.80    | 0.85      |
Overall Accuracy:85.61%

Model File:`rnn_sentiment_lstm.ipynb`  
Saved Model:`lstm_sentiment_model.keras`  
PDF Report:`reports/rnn_sentiment_lstm.pdf`

---

Tools & Technologies

| Tool                   | Purpose                               |
|:----------------------:|:-------------------------------------:|
| Python                 | Core programming language             |
| TensorFlow / Keras     | Deep learning model building          |
| Google Colab           | Cloud-based execution and GPU support |
| scikit-learn           | Evaluation metrics                    |
| Matplotlib             | Confusion matrix visualization        |
| NumPy & Pandas         | Data handling                         |

---

How to Run the Notebooks

1. Open either notebook (`.ipynb`) in Google Colab.  
2. Go to Runtime → Change runtime type → GPU.  
3. Click Runtime → Run all to execute the entire notebook.  
4. To test on your own dataset:
   - For CNN: Update the `DATA_DIR` path in the notebook to point to your dataset.  
   - For LSTM: Replace IMDb with your CSV dataset containing `text` and `label` columns.  
5. After training, model files (`.keras`) and metrics files (`.npz`) will be generated automatically.


