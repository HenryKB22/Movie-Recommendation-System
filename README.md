Movie Recommendation System
Overview
This project implements a content-based movie recommendation system using the TMDB top-rated movies dataset. The system recommends movies based on the similarity of their overviews, leveraging TF-IDF vectorization and cosine similarity to identify movies with similar themes or narratives.
Dataset
The dataset (tmdb_top_rated_movies.csv) contains metadata for 10,000 top-rated movies from The Movie Database (TMDB). Key features include:

id: Unique movie identifier
original_language: Language of the movie (e.g., 'en' for English)
overview: Textual description of the movie's plot
release_date: Movie release date
title: Movie title
popularity: Popularity score
vote_average: Average rating (0-10)
vote_count: Number of votes

Prerequisites
To run this project, you need the following Python libraries:

pandas
numpy
matplotlib
seaborn
scikit-learn

Install them using pip:
pip install pandas numpy matplotlib seaborn scikit-learn

Project Structure

Movie_recommendation_systems(Top_Rated_Movies_Loved_by_Millions).ipynb: Jupyter notebook containing the project code
tmdb_top_rated_movies.csv: Dataset file (place in the appropriate directory, e.g., /content/drive/MyDrive/Data analysis projects/)
README.md: This file

Setup

Clone or download this repository.
Ensure the dataset (tmdb_top_rated_movies.csv) is accessible in the specified path or update the file path in the notebook.
Install the required Python libraries (see Prerequisites).
Open the Jupyter notebook in an environment like JupyterLab, Google Colab, or VS Code.

Usage

Run the Jupyter notebook cells in sequence to:
Load and explore the dataset
Process movie overviews using TF-IDF vectorization
Compute cosine similarity between movie overviews
Define the recommendation function


Use the get_recommendations function to get movie recommendations. Example:get_recommendations("Schindler's List")

This will return the top 10 movies similar to Schindler's List based on overview similarity.

Example Output
For Schindler's List, the system might recommend:

Everything Is Illuminated
Resistance
The Tin Drum
The Railway Man
Defiance
Woman in Gold
A Hidden Life
The Last Metro
Blood & Gold
Inglourious Basterds

Methodology
The system uses content-based filtering:

Text Preprocessing: Movie overviews are converted to TF-IDF vectors, with English stop words removed.
Similarity Computation: Cosine similarity is calculated between all movie overviews using linear_kernel.
Recommendation: The get_recommendations function retrieves the top 10 movies with the highest similarity scores for a given movie title.

Limitations

Relies solely on movie overviews, which may miss other relevant features (e.g., genre, director).
Primarily suited for English-language movies due to dataset bias.
Short or vague overviews may reduce recommendation accuracy.

Future Improvements

Incorporate additional features like genres or cast.
Combine with collaborative filtering for a hybrid approach.
Enhance text preprocessing with lemmatization or named entity recognition.
Add visualizations of similarity scores or movie clusters.

Contributing
Contributions are welcome! Please submit a pull request or open an issue for suggestions or improvements.
License
This project is licensed under the MIT License.
Acknowledgments

The Movie Database (TMDB) for providing the dataset.
Scikit-learn for NLP and similarity computation tools.

