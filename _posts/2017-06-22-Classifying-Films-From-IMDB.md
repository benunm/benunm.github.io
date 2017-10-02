   I wanted to predict the IMDB ratings for movies on the site. IMDB has a free API, but I noticed that information is missing for a lot of films - information that can be found directly on the site. In order to work around this issue, I decided to scrape IMDB proper and avoid the API. I used requests and BeautifulSoup to do the scraping.

   I first read in a page of the top rated movies, and edited the URL in order to get the top 700 and worst 700 films. I then created a dataframe in Pandas with the film title, year, genre, IMDB rating, Metascore, and language. 

   Instead of predicting a graded score, I thought it would be cool to make this a classification project. So I added another column to my dataframe that labelled each movie as deriving from the "Best" or "Worst" lists. I used ScikitLearn's Random Forest Classifier with 6 folds and got a score of 0.72. 
   
   If I did this project over, I would have probably used more features and done more feature engineering as intuitively, I do not think that the features I fed the model could predict as well.