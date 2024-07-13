# Emotion-Recognition-Using-Multimodal-Physiological-Signals
This is a deep learning project aimed at advancing emotion recognition using multimodal physiological signals from the DEAP dataset. The project explores EEG, EOG, EMG, and GSR signals to predict emotional states categorized by the valence-arousal model. Implemented models include LSTM, GRU, and BiLSTM for effective classification and evaluation of emotional responses. This research contributes to enhancing human-computer interaction and personalized user experiences through robust emotion recognition technologies.
# Dataset
The dataset can be downloaded from http://www.eecs.qmul.ac.uk/mmv/datasets/deap/


The DEAP (Database for Emotion Analysis using Physiological Signals) dataset is a comprehensive resource for emotion analysis that includes EEG, physiological, and video signals. It is designed to facilitate research in emotion recognition by providing detailed recordings of participants' physiological responses while they watched music videos intended to elicit various emotional states.
# Pre-processed Data
For this project, we utilize the pre-processed data files from the DEAP dataset, which are available in NumPy format. The dataset comprises 32 `.dat` files, each corresponding to one participant. The data has been down sampled from the original 512 Hz to 128 Hz to reduce computational complexity while preserving essential information. Each file contains data from one of the 32 participants.
# Data Structure
Each pre-processed data file contains two arrays:
1. Data Array: A 3D array with the shape ` (40 trials, 40 channels, 8064 data points) `.
   - Trials: Each participant watched 40 one-minute music videos, constituting 40 trials.
   - Channels: The 40 channels include EEG and other physiological signals.
   - Data Points: Each trial consists of 8064 data points, reflecting the down sampled signal data.
2. Labels Array: A 2D array with the shape ` (40 trials, 4 labels) `.
-	Labels: The four labels are valence, arousal, dominance, and liking. Each trial is rated on these    dimensions, resulting in continuous values ranging from 1 to 9.
-	Valence: Measures the positivity or negativity of the emotional response.
-	Arousal: Indicates the intensity of the emotional response.
-	Dominance: Reflects the degree of control or influence the participant felt.
-	Liking: Represents the participant's overall enjoyment of the video.

# Methodology
# Modules Implemented:
1. Data Loading and Preprocessing:
Load preprocessed data files for each participant.
Segment data into epochs and assign labels based on the valence-arousal model.
2. Normalization and Scaling:
Normalize and scale segmented epochs to prepare data for model training.
Reshape data for efficient processing using deep learning models.
3. Model Training and Evaluation:
Implement LSTM, GRU, and BiLSTM models for emotion classification.
Evaluate models using metrics like accuracy, precision, recall, and F1-score on validation data

# Results
# Model Performance
1. LSTM: Accuracy = 70.69%
2. GRU: Accuracy = 73%
3. BiLSTM: Accuracy = 73%
# Confusion Matrix
1. LSTM
![image](https://github.com/user-attachments/assets/60a8eac3-1766-4273-887d-d32ff6affa7b)

2. GRU
![image](https://github.com/user-attachments/assets/113e4a29-f5b0-438f-9b0a-c857d937f883)

3. BiLSTM
![image](https://github.com/user-attachments/assets/222b8bbc-668a-44dd-adc1-ccbd18ad43bb)


