# music-recommender
This recommender system is based on a binary dataset of 355,068 music likes/dislikes collected on the PIKI MUSIC app (see https://www.piki.nyc/)

The data.csv file consists of (user_id,song_id,liked,spotify_popularity):
- liked is a binary variable that is 0 if the user disliked the song and 1 if the user liked the song
- spotify_popularity is a number between 0 and 100. See the Spotify API for more details: https://developer.spotify.com/documentation/web-api/reference/artists/get-artist/

The objective of the recommender is:
1) to maximize the accuracy of its classification of the test set. 
2) to obey the popularity constraint. The average popularity of the recommended songs should be less than or equal to the average popularity of the liked songs in the training set.
