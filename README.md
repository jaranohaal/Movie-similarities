# Movie-similarities

Movie-similarities is an NLP-based project designed to find similar movies by analyzing and comparing their plots. The project uses various Natural Language Processing (NLP) and machine learning techniques, including tokenization, stemming, TF-IDF vectorization, KMeans clustering, and hierarchical clustering. By clustering movies based on plot similarities, this project helps to identify which movies share the most in common with each other.

## Features

- **Data Preparation**: Combines plot descriptions from multiple sources and preprocesses the text.
- **Text Processing**: Uses tokenization and stemming to clean and reduce the text to its core components.
- **Feature Extraction**: Applies TF-IDF vectorization to transform movie plots into numerical vectors.
- **Clustering**: Utilizes KMeans clustering to group movies into clusters based on similarities.
- **Similarity Calculation**: Computes pairwise cosine similarities between movie plots.
- **Hierarchical Clustering**: Visualizes plot similarities using a dendrogram for better insights.
- **Movie Comparison**: Finds the most similar movie to any given movie title based on plot similarity.

## Usage
- Load the movie dataset in movies.csv.
- Process the movie plots using the provided text preprocessing functions.
- Use the clustering and similarity functions to explore relationships between movies.
- Find the most similar movie to any given title using the the_most_similar() function.

## Dendrogram Visualization

The dendrogram is a tree-like diagram that illustrates the hierarchical clustering of movies based on plot similarities. It is used to visualize how movies are grouped together according to their textual content. The height of the branches represents the distance or dissimilarity between clusters, with shorter branches indicating more similar movies.

### How It’s Used

- **Hierarchical Clustering**: After calculating cosine similarities between movie plot vectors, hierarchical clustering is applied to group the movies.
- **Dendrogram Plot**: The dendrogram shows the relationship between movies, visually depicting how they cluster into groups. By tracing the branches, you can see which movies are closely related.
- **Interpreting the Results**: Movies that merge lower in the tree are more similar to each other. This helps identify not just the closest movie pairs but also larger clusters of related movies, providing insights into the thematic similarities between films.

### Results

- The dendrogram helps reveal patterns and relationships between movies that might not be immediately obvious. For example, closely related movies can be seen grouped together, which can guide recommendations or comparisons.
- It serves as a powerful visual tool for understanding the structure of your data, making it easier to identify clusters of movies with similar plots.

![dendrogram](https://github.com/user-attachments/assets/1f80121f-64f3-4134-a7a3-33cb072021db)


## Example of usage
```python
the_most_similar("12 Angry Men")
'Mr. Smith Goes to Washington'
