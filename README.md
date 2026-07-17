# Movie-Recommendation-System
This code is a Python script that builds a web application called "Movie Recommendation System" using the Streamlit framework and the TMDB (The Movie Database) API.  

Here is a breakdown of its main components and functionality:

Initial Setup and Configuration: 
Page Configuration : The app is configured with a wide layout, titled "Movie Recommendation System", and uses a clapboard emoji (🎬) as its icon.  
API Connection: It sets up connection variables for the TMDB API, utilizing a base URL for version 3 of the API and a placeholder for an API key. 

Fetching and Selecting Genres : 
Genre Retrieval: A cached function queries the API to retrieve a list of available movie genres and creates a mapping between the genre names and their corresponding API IDs.  
User Input: The app displays a multiselect dropdown widget, allowing the user to choose one or more genres from the retrieved list. 

Fetching Movie Details : 
Credits Function: A specific function, get_movie_details, takes a movie's ID and queries the API's credits endpoint.  
Data Extraction: From the returned data, this function extracts the name of the first listed director, the first listed producer, and the names of up to three primary cast members.  

Displaying Recommendations : 
Movie Discovery: If the user has selected at least one genre, the app constructs a query to discover movies matching those genres, sorted by descending popularity.  Visual Layout: It iterates through the top 20 results, creating a visual "card" for each movie using a two-column layout.  
Movie Information: The left column displays the movie's poster image, while the right column shows the title, the plot overview, the director, the producer, and the cast. 
Default State: If no genres have been selected yet, an informational message prompts the user to select genres to begin exploring.  
