Yelp Data mining

Data source: Yelp review
API: Yelp Fusion API, Google Cloud Natural Language API

Goals and Outline:

The goal of our project is to apply clustering methods to answer the following questions that we think worthwhile to explore:
1.	What neighborhoods in a city have the best cuisine selection according to the ratings in Yelp dataset?
2.	Dose some neighborhoods in a city provide more expansive cuisines than the others?
2.	In the review of a restaurant, which kind of keywords are more likely to be mentioned?
    If a restaurant wants to improve its reviews, what should they focus on? 
This project report takes the example of reviews about "Pizza" in Boston. Three main components were done 
to solve the above questions.

1.Drawing of locations of all restaurants serves pizza in Boston shown in Google Map with Google API.

2.Geographical based clustering.
  Use K-means and GMM clustering algorithm to draw the clustering figure of restaurants. This shows the ratings and price distributions of all the restaurants.
  Silhouette Score of each clustering is calculated.

3.Classify the reviews via sentiment analysis.
  Make use of Google Cloud Natural Language API to divide review into positive and 
  negative part.
  
4.Find and plot the relationship between topics and keywords.
  Use LDA(Latent Dirichlet Allocation) to process the corpus, visualize the result by 
  PyLDAVis and Wordclouds.
  
  
Environment requirements:
-Download and install Anaconda, install Jupyter and Spyder via Anaconda.
-Register on Yelp Fusion API, get the API key.
-install required package:
 sudo pip install lda
 sudo pip install gensim
 sudo pip install PyLDAVis
 sudo pip install wordcloud
 sudo pip install bokeh
 sudo pip install sklearn
 

Running instruction:

To run the whole application, you should:
1.	run main.py in folder clustering
	This will show 	a) the plotting of all the restaurants on Google Map
			b) the K-Means and GMM clustering result for rating and price
2. 	run LDA.py in folder LDA
     	This will show  topics with key word via PyLDAVis.
3.	run sentimentDraw.py, this will show the result of sentiment Analysis of positive and negative revirew
4.      Run textBlob.ipynb, this will show the result of the review process. 