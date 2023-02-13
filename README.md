# TacoChacos

Secured third place in a hackathon (Tecoholics) conducted by LatentView Analytics. Worked in a team along with PavanPera. 

**Steps Followed for Movie Recommender System**:

**1.	Collecting Movie Data: (Scraping.ipynb)**

   	1. Here we used python library Beautiful Soup by looping over different genres limiting data to 140000 rows.

	2. Performed exploratory data analysis and removed rows with Null Values and Filtered Duplicate Rows using Movie Name as Reference.

**2.	Model Building: (Model.ipynb)**

	1. We built a Content Based Recommender System Based on NLP after a deep dive research

	2. Imported necessary libraries and data (with Necessary Columns) set we scraped

	3. The method we followed is based on Similarity of text Corpus where we vectorized the text and found similarity by using methods like Cosine Similarity, TF-IDF

	4. Extracted all the keywords row wise from columns [director, stars, plot, genres] using NLTK Library with method word_tokenize  where movie name is index for the data frame.

	5. Performed text pre-processing like lemmatization and removed other stop words.

    	6. Combined all the extracted keywords in single column with movie name as index

	7. Used CountVectorizer to Vectorize each corpus in data frame.

	8. Saved movie name list and CountVectorizer in pickle format and uploaded to GitHub.

**3.	Colab API : (API. ipynb)**

	1. Loaded the Pickle files from GitHub and other necessary libraries for Flask API

	2. Defined a function that takes input as [movie name,movie_name_list,Vector_Matrix]  and predicts top 10 similar movies based on cosine similarity of vector[ corpus ]
