
# Emotion Recognition Using CNN and LSTM

This project implements an emotion recognition system based on audio signals using Convolutional Neural Networks (CNN) and Long Short-Term Memory (LSTM) networks. The model classifies emotions from speech signals by processing audio files, extracting features, and applying deep learning techniques.


##  Table Of Contents
- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#Model_Architecture)
- [Evaluation](#Evaluation)
- [License](#License)
## Overview
This project uses a dataset of audio files to predict emotions using a hybrid model that combines CNN for feature extraction and LSTM for temporal sequence learning. The system processes audio signals by first converting them to Mel spectrograms, which are then fed into the CNN-LSTM network for classification.

## Usage
1. Prepare your dataset: Place your dataset in the correct format, ensuring it includes the paths to the audio files and the associated emotion labels.

2. Preprocess the dataset: The preprocessing includes feature extraction (Mel spectrograms) and normalization.1.

\#Example: Preprocessing the dataset \
from preprocessing import preprocess_data\
preprocess_data(dataset_path='path/to/dataset')

3. Train the model: Once the data is prepared, you can train the model:
# Example Python Code

Here’s an example of how to use the `ParallelModel` and `train_model` functions:

    ```python
    from model import ParallelModel
    from training import train_model

    model = ParallelModel(num_emotions=8)
      
    train_model(model, train_data, val_data)

4. Test the model: After training, test the model performance on the test set:

from evaluation import evaluate_model

evaluate_model(model, test_data)





## Usage

1. Prepare your dataset: Place your dataset in the correct format, ensuring it includes the paths to the audio files and the associated emotion labels.

2. Preprocess the dataset: The preprocessing includes feature extraction (e.g., Mel spectrograms) and normalization.

   ```python
   # Example: Preprocessing the dataset
   from preprocessing import preprocess_data
   preprocess_data(dataset_path='path/to/dataset')
3. Train the model: Once the data is prepared, you can train the model.
from model import ParallelModel
from training import train_model

model = ParallelModel(num_emotions=8)
train_model(model, train_data, val_data)

4. Test the model: After training, test the model's performance on the test set.

from evaluation import evaluate_model
evaluate_model(model, test_data)


## Model Architecture

The architecture consists of:

- **CNN layers** for feature extraction from Mel spectrograms.
- **LSTM layers** for sequential learning and attention mechanisms.
- **Fully connected layers** for final classification output.

### CNN + LSTM Network

The model first uses convolutional layers to extract spatial features from the Mel spectrogram. These features are then processed by a bidirectional LSTM for learning temporal patterns. An attention mechanism is employed to focus on important temporal features. Finally, the output is passed through a softmax layer for classification.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

# About the Dataset

## File Naming Convention
Each of the 7356 RAVDESS files has a unique filename. The filename consists of a 7-part numerical identifier (e.g., `02-01-06-01-02-01-12.mp4`). These identifiers define the stimulus characteristics:

### Filename Identifiers
1. **Modality**  
   - `01`: Full-AV  
   - `02`: Video-only  
   - `03`: Audio-only  

2. **Vocal Channel**  
   - `01`: Speech  
   - `02`: Song  

3. **Emotion**  
   - `01`: Neutral  
   - `02`: Calm  
   - `03`: Happy  
   - `04`: Sad  
   - `05`: Angry  
   - `06`: Fearful  
   - `07`: Disgust  
   - `08`: Surprised  

4. **Emotional Intensity**  
   - `01`: Normal  
   - `02`: Strong (NOTE: There is no strong intensity for the 'neutral' emotion)  

5. **Statement**  
   - `01`: "Kids are talking by the door"  
   - `02`: "Dogs are sitting by the door"  

6. **Repetition**  
   - `01`: 1st repetition  
   - `02`: 2nd repetition  

7. **Actor**  
   - `01` to `24`:  
     - Odd-numbered actors are male.  
     - Even-numbered actors are female.  

### Example Filename: `02-01-06-01-02-01-12.mp4`
- **Modality**: Video-only (`02`)  
- **Vocal Channel**: Speech (`01`)  
- **Emotion**: Fearful (`06`)  
- **Emotional Intensity**: Normal (`01`)  
- **Statement**: "Dogs are sitting by the door" (`02`)  
- **Repetition**: 1st repetition (`01`)  
- **Actor**: 12th actor (`12`, female)  

---

This structured format makes it easy for users to understand the dataset and its characteristics. Add it to your `README.md` and push the changes to your GitHub repository.
