# Netflix-Movies-and-TV-Shows-Clustering

The biggest provider of on-demand online streaming media and online DVD movie rentals is Netflix. Marc and Reed founded it on August 29, 1997, in Los Gatos, California. Its 69 million users reside in more than 60 nations and watch more than 100 million hours of TV and videos each day. With access to TV shows, documentaries, and feature films in a broad range of genres and languages, Netflix is the top global provider of online entertainment. These straightforward, engaging, and exciting visualisations were made as a result of my curiosity to analyse the Netflix platform's newly released material in order to identify demographic groups that shared interests.

As of 2019, the Netflix content included in this dataset comprises of TV shows and films. The information was gathered from the independent Netflix search engine Fixable. The number of TV shows available on Netflix has almost tripled since 2010, according to an interesting study that was published in 2018. Since 2010, the number of movies available on the streaming service has dropped by more than 2,000, whereas the number of TV programmes has nearly tripled. Investigating what additional insights can be drawn from the same dataset will be fascinating. Many intriguing results can be obtained by combining this dataset with other external datasets, such as IMDB ratings and rotten tomatoes.

Dataset information:

1. show_id : Unique ID for every Movie / Tv Show

2. type : Identifier - A Movie or TV Show

3. title : Title of the Movie / Tv Show

4. director : Director of the Movie

5. cast : Actors involved in the movie / show

6. country : Country where the movie / show was produced

7. date_added : Date it was added on Netflix

8. release_year : Actual Releaseyear of the movie / show

9. rating : TV Rating of the movie / show

10. duration : Total Duration - in minutes or number of seasons

11. listed_in : Genere

12. description: The Summary description

# conclusion:
1.In this project, we worked on a text clustering problem where in we had to classify/group the Netflix shows into certain clusters such that the shows within a cluster are similar to each other and the shows in different clusters are dissimilar to each other.

2.The dataset contained about 7787 records, and 12 attributes. We began by dealing with the dataset's missing values and doing exploratory data analysis (EDA).

3.It was found that Netflix hosts more movies than TV shows on its platform, and the total number of shows added on Netflix is growing exponentially. Also, majority of the shows were produced in the United States, and the majority of the shows on Netflix were created for adults and young adults age group.

4.Once obtained the required insights from the EDA, we start with Pre-processing the text data by removing the punctuation, and, stop words. This filtered data is passed through TF - IDF Vectorizer since we are conducting a text-based clustering and the model needs the data to be vectorized in order to predict the desired results.

5.It was decided to cluster the data based on the attributes: director, cast, country, genre, and description. The values in these attributes were tokenized, preprocessed, and then vectorized using TFIDF vectorizer.

6.Through TFIDF Vectorization, we created a total of 20000 attributes. We used Principal Component Analysis (PCA) to handle the curse of dimensionality. 4000 components were able to capture more than 80% of variance, and hence, the number of components were restricted to 4000. We first built clusters using the k-means clustering algorithm, and the optimal number of clusters came out to be 6. This was obtained through the elbow method and Silhouette score analysis.

7.Then clusters were built using the Agglomerative clustering algorithm, and the optimal number of clusters came out to be 12. This was obtained after visualizing the dendrogram.

8.A content based recommender system was built using the similarity matrix obtained after using cosine similarity. This recommender system will make 10 recommendations to the user based on the type of show they watched.
