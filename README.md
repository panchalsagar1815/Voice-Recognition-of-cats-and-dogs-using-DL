# Voice-Recognition-of-cats-and-dogs-using-DL

# **Project Title: Voice Recognition of Cats and Dogs Using Deep Learning**

**Overview:**
The "Voice Recognition of Cats and Dogs using Deep Learning" project focuses on developing an innovative system that can classify different breeds of cats and dogs based on their unique vocalizations. By employing state-of-the-art deep learning techniques, the project not only achieves accurate voice classification but also provides valuable insights into the performance of the model.

**Key Features:**

1. **Data Collection and Cleaning:**
   - Curated a diverse dataset containing voice inputs from various breeds of cats and dogs.
   - Implemented robust data cleaning techniques to remove noise and inconsistencies in the audio recordings.
   - Utilized auto-tuning to enhance the quality and standardization of the voice data.

2. **Input Pipeline and Labeling:**
   - Created an efficient input pipeline to handle the loading and processing of voice data.
   - Labeled each sample of data as either cat voice, dog voice, or reserved for testing purposes.
   - Ensured a balanced distribution of samples to prevent bias in the model training.

3. **Model Architecture:**
   - Developed a Sequential model architecture with key layers such as resizing, normalization, convolutional layers, dropout, max-pooling, and dense layers.
   - The model was designed to process 32x32 mono-channel audio spectrograms, capturing essential features for voice classification.
   - Achieved a total of 3,250,822 parameters, making the model capable of learning intricate patterns.

4. **Model Performance:**
   - Evaluated the model on a test set and obtained precision, recall, and f1-score metrics.
   - Achieved an overall accuracy of 87%, demonstrating the model's effectiveness in distinguishing between cat and dog vocalizations.
   - The precision, recall, and f1-score metrics provide a comprehensive view of the model's performance for each class.

**Model Architecture:**
```plaintext
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
resizing (Resizing)          (None, 32, 32, 1)         0         
_________________________________________________________________
normalization (Normalization (None, 32, 32, 1)         3         
_________________________________________________________________
conv2d (Conv2D)              (None, 30, 30, 32)        320       
_________________________________________________________________
dropout (Dropout)            (None, 30, 30, 32)        0         
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 28, 28, 128)       36992     
...
dense_2 (Dense)              (None, 3)                 51        
=================================================================
Total params: 3,250,822
Trainable params: 3,250,819
Non-trainable params: 3
```

**Model Performance Metrics:**
```plaintext
precision    recall  f1-score   support

           0       0.89      0.87      0.88        39
           1       0.83      0.86      0.84        28

    accuracy                           0.87        67
   macro avg       0.86      0.86      0.86        67
weighted avg       0.87      0.87      0.87        67
```

**Conclusion:**
The successful implementation of this voice recognition model demonstrates its potential applications in pet monitoring, smart homes, and animal behavior research. Future work may include expanding the dataset to include more breeds and refining the model for real-world deployment.
