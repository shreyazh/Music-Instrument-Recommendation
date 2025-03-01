# Hybrid AI Music Instrument Recommendation System

## Overview
This project implements a **hybrid AI-based recommendation system** for musical instruments. It combines:
- **Collaborative Filtering (CF):** Predicts user preferences based on past ratings.
- **Content-Based Filtering (CBF):** Analyzes textual reviews for sentiment and similarity.
- **Hybrid Model:** Merges CF and CBF to generate personalized recommendations.

## Features
- **Collaborative Filtering:** Uses Singular Value Decomposition (SVD) from the `Surprise` library.
- **Sentiment Analysis:** Extracts insights from user reviews using VADER.
- **Content Similarity:** Applies TF-IDF and cosine similarity for better recommendations.
- **Hybrid Scoring:** Combines CF predictions, content similarity, and sentiment scores.

## Dataset
A synthetic dataset `music_reviews.csv` is included with:
- `instrument_id`: Unique ID for musical instruments.
- `user_id`: Unique user identifier.
- `rating`: User-provided rating (1-5 scale).
- `review`: User feedback text.

## Installation
```bash
pip install pandas numpy surprise nltk scikit-learn
```

## Usage
1. **Load Data:** Ensure `music_reviews.csv` is in the working directory.
2. **Run the Model:**
```python
from hybrid_recommender import hybrid_recommend
recommendations = hybrid_recommend(user_id=123, instrument_id=456)
print(recommendations)
```

## Customization
- Adjust **weights** for CF, sentiment, and content similarity.
- Train on a **larger dataset** for better accuracy.
- Modify **TF-IDF parameters** for text processing.

## Future Enhancements
- Integrate **deep learning** for better review understanding.
- Expand recommendation logic with **user demographics**.
- Deploy as a **web API** using Flask or FastAPI.

## License
This project is open-source and available under the MIT License.

