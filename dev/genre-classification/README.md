# Project: Genre Classification

## Goal
Development of a genre classifier to predict the genre of a given track based on the audio features.

## Data Collection
Data is collected via Spotify API.

## Genre
Spotify has a wide variety of genres. As a PoC, we decided to develop a classifier for a small set of genres:
- rap, rock, metal, blues, jazz, classical, funk, techno, electronic, r&b

## TODOs
| ToDo                                                                                      | State |
|-------------------------------------------------------------------------------------------|-------|
| Initial training                                                                          | ✓     |
| Find out more info about genre tree structure of Spotify                                  | ✓     |
| Train with more data (1000 tracks per genre)                                              | ✓     |
| Train with different set of features (popularity, duration, bpm, liveness, loudness, key) | ✓     |
| Visualize results                                                                         | ✓     |
| Collect data: get 1000 unique tracks per genre                                            |       |
| Hyperparameter tuning (especially RandomForest & SVC)                                     | 🚧    |
| Usecase: multiclass classifier                                                            |       |
| Usecase: create a model with prediction value                                             |       |
