
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
