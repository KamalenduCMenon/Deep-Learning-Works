# Study of Hyperparameter for LSTM and SimpleRNN Model for Text Classification

---

This project focuses on analyzing how different hyperparameters impact the performance of Recurrent Neural Network (RNN) and Long Short-Term Memory (LSTM) models in a text classification task. The IMDb movie reviews dataset is used for training and evaluating sentiment classification performance.

## Objective

The goal is to understand how model architecture and training parameters such as state dimensions, dropout rate, learning rate, batch size, and number of epochs affect model accuracy and generalization. Both RNN and LSTM are evaluated under various configurations.

## Dataset and Word Embedding

- **IMDb Dataset:** Contains 50,000 labeled movie reviews (positive or negative).  
- **Preprocessing:** Includes text cleaning (removing HTML tags, punctuation, etc.), lowercasing, and tokenization.  
- **Embedding:** Utilizes 100-dimensional GloVe vectors to map words to dense vector representations.

## Model Architecture

- Implemented in **TensorFlow** and **Keras**.
- Common architecture: Embedding Layer → RNN or LSTM → Global Average Pooling → Dropout → Dense (Sigmoid).
- Trained using Binary Crossentropy loss and Adam optimizer.

## Hyperparameter Tuning

Hyperparameters tuned using **RandomizedSearchCV**:
- State dimensions: `[20, 50, 100, 200, 500]`
- Learning rates: `[0.01, 0.001, 0.0001]`
- Dropout rates: `[0.2, 0.3, 0.5]`
- Batch sizes: `[32, 64, 128]`
- Epochs: `[5, 10, 15]`

Tuning helps find the most effective combinations to improve test accuracy while avoiding overfitting.

## Results

- **LSTM Best Accuracy:** ~88.9% with state_dim=100, learning_rate=0.01, dropout=0.2, batch_size=128  
- **RNN Best Accuracy:** ~85.8% with state_dim=200, learning_rate=0.001, dropout=0.3, batch_size=64  
- Validation loss and accuracy trends show the importance of balanced complexity and regularization.

## Conclusion

- Preprocessing and embeddings significantly improve model input quality.
- LSTM generally outperforms vanilla RNN due to better long-term dependency handling.
- Hyperparameter tuning is essential to achieve optimal performance.
- Overfitting is observed with large models and insufficient regularization, highlighting the need for careful tuning.

---


