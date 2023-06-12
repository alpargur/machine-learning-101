# Project: Genre Classification

## Goal
Development of a genre classifier to predict the genre of a given track based on the audio features.

## Data Collection
Data is collected via Spotify API.

## Genre
Spotify has a wide variety of genres. As a PoC, we decided to develop a classifier for a small set of genres:
- rap, rock, metal, blues, jazz, classical, funk, techno, electronic, r&b

## Getting Started
- Make sure you have package `virtualenv` -> `pip show virtualenv`
- If not open terminal and execute following lines
```bash
$ virtualenv env
$ source virtualenv/bin/activate
$ pip install -r requirements.txt
$ deactivate # to shutdown the virtual environment
```

## Notes
- We have retrieved different amounts of track for each genre and created separate training and tuning files. Below you find details of files:
  - `data-collection` is responsible for collecting tracks and features.
  - `data-exploration` extracts overview about the data we are handling.
  - `initial_datatraining` trains models with 100 tracks for each genre.
  - `initial_datatraining_1k` training models with 1000 unique tracks for each genre.
  - `hyperparameter-tuning-RFC` optimizing models with 1000 tracks for model RandomForestClassifier.
  - `hyperparameter-tuning-SVC` optimizing models with 100 tracks for model SuperVectorClassifier.
  - `multiclass-classifier-1k` training of multiclass classifiers for 1000 unique tracks for each genre.
  - `multiclass-classifier-soft-voting-ensemble` training of an ensemble learning model consisting of binary classifiers, 1000 unique tracks for each genre.
- Collected data and exported model performances can be found in `./data` directory.


## TODOs
| ToDo                                                                                      | State |
|-------------------------------------------------------------------------------------------|-------|
| Initial training                                                                          | ✓     |
| Find out more info about genre tree structure of Spotify                                  | ✓     |
| Train with more data (1000 tracks per genre)                                              | ✓     |
| Train with different set of features (popularity, duration, bpm, liveness, loudness, key) | ✓     |
| Visualize results                                                                         | ✓     |
| Collect data: get 1000 unique tracks per genre                                            | ✓     |
| Hyperparameter tuning (especially RandomForest & SVC)                                     | ✓     |
| Usecase: multiclass classifier                                                            | ✓     |
| Usecase: create a model with prediction value                                             | ✓     |