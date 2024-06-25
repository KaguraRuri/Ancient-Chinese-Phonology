# ACP: Automatic Reconstruction of Ancient Chinese Pronunciations

This repository contains the source code for the paper **"Automatic Reconstruction of Ancient Chinese Pronunciations"**.

## Overview
This project aims to reconstruct ancient Chinese pronunciations using a transformer-based model, incorporating both glyph and temporal features. The dataset, ACP (Ancient Chinese Phonology), consists of digitized phonology rules for a large number of Chinese characters spanning multiple historical periods.

We have also created a demo website where you can see the predicted future pronunciations of some Chinese characters using our model. Check it out at [Ancient Chinese Demo](http://47.97.123.246:8080/).

## Requirements
To run the code, you'll need the following dependencies:
- `python`: 3.7.6
- `pytorch`: 1.5.0
- `transformers`: 3.5.0

You can install the required packages using:
```bash
pip install -r requirements.txt
```

## Dataset
The dataset used in this project is the Ancient Chinese Phonology (ACP) dataset, which includes phonological data for a substantial number of Chinese characters.

## Directory Structure
The repository is structured as follows:
```
├── dataset/                # Directory containing the dataset
├── train/               # Directory containing training scripts
├── utils/               # Utility scripts and helper functions
├── requirements.txt     # Required Python packages
├── README.md            # This README file
└── LICENSE              # License file
```

## Training
To train the model, follow these steps:
1. Navigate to the `train` directory:
    ```bash
    cd train
    ```
2. Run the training script:
    ```bash
    python train.py
    ```

## Demo Results
Below are some examples of the predicted pronunciations for various Chinese characters across different historical periods:

| Character | MiddleTang | LateTang | Song      | Yuan          | MingQing      | Modern    | AD2300        |
| --------- | ---------- | -------- | --------- | ------------- | ------------- | --------- | ------------- |
| **觊**    | k - i -    | k - i -  | k - i -   | **k - əi -**  | **kʰ - i -**  | ʨ - i -   | **ʨʰ - əi -** |
| **涶**    | tʰ u ɑ -   | tʰ u ɑ - | tʰ u ɔ -  | **tʰ u ɔ -**  | **tʰ u o -**  | tʰ u o -  | **tʰ u a -**  |
| **惭**    | ʣ - ɑ m    | z - a m  | ʦʰ - a m  | **ʦʰ - a m**  | **ʦʰ - a n**  | ʦʰ - a n  | **tʰ - a n**  |
| **亟**    | kʰ - i -   | kʰ - i - | kʰ - i -  | **tʰ - i -**  | **t - i -**   | ʨ - i -   | **ʨʰ - i -**  |
| **调**    | d i æu -   | d i æu - | tʰ i æu - | **tʰ i æu -** | **tʰ i ɑu -** | tʰ i ɑu - | **tʰ i ɔu -** |
| **禾**    | ɣ u ɑ -    | ɦ u ɑ -  | h u ɔ -   | **h ɛ ɔ -**   | **x ɛ e -**   | x - ɤ -   | **x - i -**   |
| **眈**    | d - ɑ m    | d - a m  | tʰ - a m  | **t - a n**   | **t - a ɲ**   | t - a n   | **t - a ŋ**   |
| **颐**    | j - i -    | j - i -  | j - i -   | **j - ɛ -**   | **j - i -**   | j - i -   | **j - i -**   |
| **淑**    | ʑ i o k    | ʑ - u k  | ɕ - u k   | **ɕ - o -**   | **ʂ - o -**   | ʂ - u -   | **ʃ - u -**   |
| **卧**    | ŋ u ɑ -    | ŋ u ɑ -  | ŋ u ɔ -   | **w - ɔ -**   | **w u ɔ -**   | w - o -   | **w - ɔ -**   |
| **畔**    | b u ɑ n    | b u a n  | p u a n   | **pʰ u a n**  | **pʰ - a n**  | pʰ - a n  | **pʰ - a n**  |
| **穹**    | kʰ i o ŋ   | kʰ - u ŋ | kʰ - u ŋ  | **ʨʰ - u ŋ**  | **ʂ - y ŋ**   | ʨʰ - y ŋ  | **ɣ - ua ŋ**  |
| **醉**    | ʦ i ui -   | ʦ i ui - | ʦ - ɿ -   | **ʦ - uə -**  | **ʦ - uæ -**  | ʦ u ei -  | **ʦ ɚ ei -**  |
| **曾**    | ʣ - ə ŋ    | z - ə ŋ  | ʦʰ - ə ŋ  | **ʦ - e ŋ**   | **ʦ - i ŋ**   | ʦ - ə ŋ   | **ʦ - u ŋ**   |
| **划**    | ɣ u ɐ k    | ɦ u ə k  | h u ə k   | **h u a k**   | **h u ɑ -**   | x u ɑ -   | **x u a -**   |
| **殂**    | ʣ - u -    | z - u -  | ʦʰ - u -  | **ʦ - u -**   | **ʦ - u -**   | ʦʰ - u -  | **ʧ - u -**   |
| **菱**    | l i ə ŋ    | l i ə ŋ  | l i ə ŋ   | **l - i ŋ**   | **l - i ŋ**   | l - i ŋ   | **l - a ŋ**   |
| **岚**    | l - ɑ m    | l - a m  | l - a m   | **l - a n**   | **l - a n**   | l - a n   | **l - a ŋ**   |
| **攻**    | k - u ŋ    | k - u ŋ  | k - u ŋ   | **k - u ŋ**   | **k - u ŋ**   | k - u ŋ   | **kʰ - u ŋ**  |
| **盲**    | m - ɐ ŋ    | m - ɐ ŋ  | m - ɐ ŋ   | **m - a ŋ**   | **m - a ŋ**   | m - a ŋ   | **m - æ ŋ**   |
| **觉**    | k - ɔ k    | k - ɔ k  | k - ea k  | **k - ea k**  | **ʨ - ɛ -**   | ʨ y ɛ -   | **ʨ u ɛ -**   |
| **莺**    | ʔ - ɐ ŋ    | ʔ - ɐ ŋ  | j - ɐ ŋ   | **j - ɐ ŋ**   | **j - i ŋ**   | j - i ŋ   | **j - i ə**   |
| **诂**    | k - u -    | k - u -  | k - u -   | **k - u -**   | **k - u -**   | k - u -   | **kʰ - u -**  |
| **荏**    | ȵ - i m    | r i ə m  | r - i m   | **r - ə m**   | **r - ə n**   | ɻ - ə n   | **ɻ - æ n**   |
| **核**    | ɣ - ɐ k    | ɦ - ə k  | h - ə k   | **f - ə k**   | **pʰ - ə k**  | x - ɤ -   | **s - ɔ -**   |
| **郝**    | ɕ i ɐ k    | ɕ i ə k  | ɕ - i t   | **ɕ - i tʰ**  | **x - au -**  | x - ɑu -  | **x - ɑ -**   |
| **射**    | j i a -    | j i a -  | j i a -   | **j i a -**   | **ʂ - ɛ -**   | ʂ - ɤ -   | **ʂ - ə -**   |
| **刊**    | kʰ - ɑ n   | kʰ - a n | kʰ - a n  | **kʰ - a n**  | **kʰ - a n**  | kʰ - a n  | **kʰ - æ n**  |
| **惹**    | ȵ i a -    | r - a -  | r - a -   | **ɽ - e -**   | **ɽ - e -**   | ɻ - ɤ -   | **ɻ - e -**   |
| **厕**    | ʧʰ - i -   | ʧʰ - i - | ʦʰ - ɿ -  | **ʦ - e -**   | **ʦ - ɤ -**   | ʦʰ - ɤ -  | **ʦ - e -**   |

