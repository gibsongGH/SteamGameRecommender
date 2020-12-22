# Steam Game Recommender
Video Game Recommender from Steam website data


This second capstone project through Springboard takes player reviews from the video game hositing company Steam and makes recommendations.  Files are acquired from steampowered.com utilizing the steamreviews library on pypi.org.  Further game information was pulled from steamspy.com, a website dedicated to tracking video game sales.

748 game IDs
2.3M player IDs
3.3M reviews

Instead of 5-point ratings typically seen in movie recommenders, the key feature is a binary vote indicating liked or disliked.  The primary recommendations are built from the cosine similarity of up-votes between games, then ranking the closest matching games to what users have already played.  This work leverages the Collaborative Filtering with Python post by Salem Marafi and updates from the Item-Item Collaborative Filtering with Binary or Unary Data post by Viktor Kohler.

http://www.salemmarafi.com/code/collaborative-filtering-with-python/

https://medium.com/radon-dev/item-item-collaborative-filtering-with-binary-or-unary-data-e8f0b465b2c3

Player text reviews were scored for sentiment through VADER and incorporated into the game rankings, then further filtered by the player's preferred video game genre.
