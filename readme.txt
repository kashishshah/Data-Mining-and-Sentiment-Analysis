*********************************** CONFIGURATION ***********************************

== API Accounts ==

In order to use the New York Times and Twitter Sentiment Analysis application, a user must have registered an account to use the Twitter API, New York Times API and The Movie Database (TMDB) API.  Registering with these services will provide the user with the authentication keys and tokens required to make the API calls in the application code.


Information pertaining to the Twitter API can be found here:

\href{https://developer.twitter.com/en/docs/ads/general/guides/getting-started}{Getting Started with the Twitter API}.


The information for NY Times API can be found here:

\href{https://developer.nytimes.com/}{Get Started with the New York Times API}.

Similarly, the information for TMDB API can be found here:

\href{https://developers.themoviedb.org/3}{Get Started with the TMDB API}.

== Authentication File ==

Once accounts are setup with the two API services, the keys and tokens will need to be stored in JSON format in a file called credentials.json.  This file should be placed in the same directory as the application's Jupyter Notebook.  A file containing the keys currently exists in the zip file.
The file must contain the following key value pairs all at the initial level in the JSON file.

KEY		VALUE

ACCESS_KEY	Twitter API key
ACCESS_SECRET	Twitter API secret Key
CONSUMER_KEY	Twitter API token
CONSUMER_SECRET	Twitter API secret token
IBM_TONE_KEY	IBM Tone Analyzer key
NYT_BOOK_KEY	New York Times book review key
NYT_MOVIE_KEY	New York Times movie review key
TMDB_MOVIE_KEY	The Movie Database key


== Data Subdirectory ==

Lastly, the data subdirectory must be included with the Jupyter Notebook.  This folder, included in the submission, contains csv data of approximately 4800 movies in a file named tmdb_movies.csv and book titles and its reviews in Goodreads.csv file.

******************************** Running the Code ********************************

After all of the configuration steps have been completed, the Juypiter Notebook is ready to be run.  In order to start the application, all modules in the Jupyter Notebook must be run in order.  The final module starts the Plotly application and will then be used to interact with the application by requesting user inputs and generating plots as output.

Once the application is running, the user can supply input using the dropdown menu on the left and insert the query in textbook and click submit button to view the plots.

*********************************** Limitations ***********************************

== Plotly ==

The plotly plotting library takes almost three seconds to perform real-time update in the graphs when user input changes. Also, it is mandatory to initialize some of the widget parameters in plotly.

== Twitter API ==

Twitter Standard API provides tweets of past 7 days. The issue arises when the input of the user contains a movie/book which is somewhat old because it may be possible that there have been no tweets related to that movie/book in the recent time.