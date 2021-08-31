### MVP:

The focus of the project was to explore whether game genres be classified from games screenshots using deep learning techniques.

The following steps have been completed so far:

- Download screenshots of games from the steam store API (10,000 images)
- [`tf.keras.preprocessing.image_dataset_from_directory`](https://www.tensorflow.org/api_docs/python/tf/keras/utils/image_dataset_from_directory) is used to load images from directory.
- Obtain genres for games through the steam spy API
- The following genres are to be classified: ['anime', 'automobile sim', 'difficult', 'fantasy', 'fps', 'funny', 'hack and slash', 'horror', 'mmorpg', 'platformer', 'puzzle', 'rts', 'sandbox', 'sci-fi', 'stealth', 'story rich', 'survival', 'third person', 'turn-based strategy', 'zombies']
- A sequential neural network with VGG and 2 additional dense layers was created. (Categorical Cross Entropy as loss function )



With 3 Epochs, accuracy of .32 was achieved on validation set.



Future Steps:

- More epochs with the use of GPUs
- Add dense layers
- Add conv layers
- Change metrics from accuracy to f1 score
- Re-explore how genres are assigned to games, right now there is too much overlap between genres
- Implement multi labeller, instead of classification
