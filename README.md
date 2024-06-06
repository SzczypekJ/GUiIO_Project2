# Music Genre Classification using Convolutional Neural Networks

## Project Overview

This project aims to classify music genres using various models based on Convolutional Neural Networks (CNNs). The models take spectrograms and Mel-Frequency Cepstral Coefficients (MFCCs) generated from audio files as input and output the music genre of the track.

## Team Members

- **Łukasz Gakan**
- **Piotr Mamos**
- **Dawid Maziarski**
- **Julia Nowak**
- **Michał Rola**
- **Jakub Szczypek**
- **Szymon Szewczyk**
- **Łukasz Szyszka**
- **Adam Złocki**


## Introduction

Machine learning is one of the fastest-growing technologies, applicable in many fields. One of its key advantages is the ability to automatically detect patterns in training data, enabling the creation of accurate predictive models. Applications include personalized advertising, content recommendations, and route optimization in transportation.

This project focuses on creating and comparing various music genre classifiers using CNN techniques. The models use spectrograms and MFCC parameters generated from audio files to classify the music genre.

## Technologies and Tools

- **Python 3.11**: The primary programming language used for implementation.
- **Libraries**: Keras, Librosa, Matplotlib, NumPy, scikit-learn.

## Dataset

The GTZAN dataset from Kaggle was used for training and testing. It consists of 1000 tracks, each 30 seconds long, divided into 10 genres: blues, classical, country, disco, hip-hop, jazz, metal, pop, reggae, and rock.

## Models

### Spectrogram-Based Model

- **Architecture**: MobileNet pre-trained on ImageNet, adapted for music genre classification.
- **Training Process**:
  - Initial training with only the output layer.
  - Subsequent training with half of the MobileNet layers unlocked.
- **Results**: Achieved an accuracy of 0.88 on the test set with a loss of 0.5021.

### MFCC-Based Model

- **Custom CNN Architecture**: Designed specifically for MFCCs.
- **Training Process**: 
  - Used 128 batch size and 150 epochs.
  - Early stopping and checkpointing were implemented.
- **Results**: Achieved an accuracy of 0.72 on the test set with a loss of 1.48.

## Application

A GUI was developed to facilitate the use of the models. It allows users to upload audio files and classify them using the trained models.

### How to Run the Application

1. **Install Python**: Ensure that you have Python 3.11 or later installed on your system.

2. **Clone the Repository**: 
    ```sh
    git clone https://github.com/SzczypekJ/GUiIO_Project2.git
    cd GUiIO_Project2
    ```

3. **Create a Virtual Environment**:
    ```sh
    python -m venv venv
    source venv/bin/activate   # On Windows use `venv\Scripts\activate`
    ```

4. **Install Dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

5. **Run the Application**:
    Navigate to the `DL_GUI` directory and run the application script.
    ```sh
    cd DL_GUI
    python mainwindow.py
    ```

6. **Using the Application**:
    - Upon running the script, a GUI window should appear.
    - You can upload an audio file in `.mp3` or `.wav` format.
    - The application will display the predicted music genre along with confidence percentages.