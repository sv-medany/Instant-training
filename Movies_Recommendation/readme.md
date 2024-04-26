# Movie Recommendation System

This project implements a movie recommendation system using cosine similarity based on movie overviews and genres. It utilizes a dataset containing movie titles, overviews, and genres.

## Functionality

The movie recommendation system operates as follows:

1. **Data Preprocessing**: The system first reads the dataset containing movie titles, overviews, and genres. It then filters the dataset to include only relevant columns, such as movie ID, title, overview, and genre. These columns are combined to create a new feature called `filter_category`, which represents a combination of the movie overview and genre.

2. **Vectorization**: Using the CountVectorizer from scikit-learn, the system converts the textual data in the `filter_category` feature into numerical vectors. This process involves tokenizing the text, converting it to lowercase, removing stopwords, and creating a bag-of-words representation of the data.

3. **Cosine Similarity**: After vectorizing the data, the system computes cosine similarity between pairs of movies based on their vector representations. Cosine similarity measures the cosine of the angle between two vectors and ranges from -1 to 1, where higher values indicate greater similarity.

4. **Recommendation**: To recommend movies similar to a given movie, the system first identifies the index of the target movie in the dataset. It then calculates the cosine similarity between the target movie and all other movies. Finally, it selects the top similar movies based on their cosine similarity scores and presents them as recommendations.

## Usage

1. Clone the repository: `git clone https://github.com/sv-medany/movie-recommendation.git`
2. Ensure you have Python and the required libraries installed.
3. Run the provided Python script to load the dataset and create the recommendation system.
4. Use the `recommend_movie` function to get recommendations for a specific movie.

## Example

```python
from movie_recommendation import recommend_movie

# Get recommendations for a movie
recommend_movie("Superman")

