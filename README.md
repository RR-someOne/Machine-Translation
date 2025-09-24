# Neural Machine Translation Project

## Overview
This repository contains the source code for a Neural Machine Translation (NMT) system. The project focuses on building a robust and high-performance model for translating text between a specific language pair. The core of the system is a Transformer-based architecture, which has become the de-facto standard for sequence-to-sequence tasks like machine translation.

## Features
Transformer Architecture: Implements a full Transformer model (as described in "Attention Is All You Need") for state-of-the-art translation quality.

Tokenization & Preprocessing: Uses a subword tokenization algorithm (e.g., SentencePiece or BPE) to handle out-of-vocabulary words and improve model efficiency.

Training & Evaluation Scripts: Includes scripts for training the model from scratch on a parallel corpus and for evaluating its performance using metrics like BLEU.

Inference Engine: Provides a simple and efficient way to perform translations on new text.

## Getting Started
Follow these steps to get the project up and running on your local machine.

## Prerequisites
You will need the following installed:

Python 3.7+

pip (Python package installer)

## Installation
Clone the repository:

git clone [https://github.com/RR-someOne/Machine-Translation.git](https://github.com/RR-someOne/Machine-Translation.git)
cd Machine-Translation

## Create and activate a virtual environment:

python3 -m venv venv
source venv/bin/activate

Install the required libraries:

pip install -r requirements.txt

Note: The requirements.txt file should contain all necessary libraries like torch, transformers, numpy, sentencepiece, etc.

Data Preparation
This project requires a parallel corpus for training. You can use a standard dataset like the WMT'14 English-to-French dataset.

Place your parallel data files (e.g., train.en, train.fr, dev.en, dev.fr) in a data/ directory.

Run the data preprocessing script to tokenize and prepare the data for training.

python scripts/prepare_data.py

Training the Model
To train the model, use the train.py script. You can adjust hyperparameters and configuration settings in the config.yaml file.

python train.py --config configs/transformer_base.yaml

Training checkpoints and logs will be saved to the checkpoints/ directory.

Translation & Inference
Once the model is trained, you can use the translate.py script to translate new text.

# Translate a single sentence
python translate.py --text "This is an example sentence."

# Translate a text file
python translate.py --file "path/to/input.txt" --output "path/to/output.txt"
<img width="683" height="493" alt="Screenshot 2025-09-24 at 9 21 44 AM" src="https://github.com/user-attachments/assets/535d31d8-a034-48b5-baf7-d1f95b777827" />

