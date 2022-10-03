# Game Genres Labeller - Using Deep Learning Techniques

*Matteo Fortier*

## Design

A new video streaming platform wants to be able to better/automatically categorize sub genres of gaming videos. They want to be able to categorize gaming videos based on the games' genres. This would allow them to better recommend users videos based on the video they are currently watching, and increase watch time. Thus, it is valuable to explore whether games can be classified based on screenshots alone, which the streaming platform would have access to.

## Data

 The Steam Store API data was used for this project. The dataset includes information on video games found on the steam store. The two important features found in the dataset are the genres of games and the urls to game screenshots. Together, the two features can be used as feature and target variables to classify game genres from their screenshots. There are 40,000 games, however only 800 (games with >1,000,000 owners) were selected as each game may have multiple screenshots. 10,000 images were collected by the end of the process. 

There were ~13 genres initially, however the genres that had little data were removed, as well as the genres that didnt make sense (Free to Play).

Finally there were 9 labels that a game could have: Sports, Adventure, Action, Simulation, Massively Multiplayer, Strategy, Racing, Casual, RPG.

## Algorithms

***Deep Learning***

- tf.data library was used to create custom tensor generators for multi-label data.
- Transfer Learning Models Explored: VGG, MobileNet, NasNet - VGG was selected as it performed the best
- Data Augmentation to reduce overfitting - RandomFlip, RandomRotate, RandomContrast, RandomZoom -> reduced as it poorly affected model results.
- Dropout to reduce overfitting -> reduced as it poorly affected model results
- Early stopping to reduce overfitting
- ReduceLRonPlateau -> improved model perfomance
- 3 Additional Dense Layers with 200, 100, 100 units. (relu)

***Techniques for MultiLabel Classification***

- Macro-F1 (with threshold as parameter, default 0.5) used as metric
- Soft-Macro-F1(with threshold as parameter, default 0.5) used as loss function
- Output layer consists of dense layer with n_classes (9) nodes, with sigmoid activation. 

## Tools

- Python, pandas, NumPy, SciPy, scikit-learn
- Google Cloud Platform
- Swifter (Dask Pandas)
- VGG, MobileNet, NasNet
- Google Colab
- Tensorflow, Keras
- Tf.Data

## Communication

The project used powerpoint for the presentation and the python visualisation libraries for the visuals. 

[embed]presentation.pdf[/embed]
