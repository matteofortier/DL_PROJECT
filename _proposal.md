### Project Proposal: Game Genre Classification based on screenshots/images of games

**Framing Question:** Can game genres be classified from games screenshots using deep learning techniques?

**Purpose and Need:** 

A new video streaming platform wants to be able to better/automatically categorize sub genres of gaming videos. They want to be able to categorize gaming videos based on the games' genres. This would allow them to better recommend users videos based on the video they are currently watching. Thus, it is valuable to explore whether games can be classified based on screenshots alone, which the streaming platform would have access to.

**Data Description:**

Steam Store API 

The steam store API provides screenshots/images for each game on their store. There are over 40000 games, however only a few games will need to be explored as each game may have multiple images/screenshots available.

**Tools:**

- Python, pandas, NumPy, SciPy, scikit-learn
- Probably a GCP compute unit with a GPU
- Keras, Tensorflow
- Transferred learning image classifying data

**MVP Goal:**

A baseline model able to predict the genres of games based on screenshot.
