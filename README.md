# imdb_and_chill   

**An application using computer vision to help you decide what movie / TV show to watch next**   
   
Netflix, Hulu, HBO Go, HBO Now, HBO Max, Disney +, Apple TV +, Amazon Prime Video, Youtube TV and I am forgetting a few. You just wanted to Netflix and chill. Now you have so much choice that you can't even focus on the chilling anymore…   
   
Who didn't spend at least a half hour trying to decide what to watch? Browsing endlessly the catalog. So much options. Yet so little information about the titles… That you end up "IMDBing" the movies/tv shows before deciding. In the world of Alexa, voice and image activated services, manually doing the process of searching IMDB is just so 2018.   
   
The concept is simple. Simplicity is valuable. You aim the camera of your phone at the screen, and you can visualize the IMDB score of the movie/TV show directly on your phone's screen.   
   
I decomposed the process in three steps:   

**Step 1: leverage AWS**   
The app needs two things: first, to recognize that there is a TV (true, you could be streaming on a different screen, but as I said, I like simplicity) and if there is a screen, locate and extract the text within the images (text which is the title of the movie/TV show - once again, there are no protections against misuse but it's a small project);   

**Step 2: leverage Google**   
To give you the rating, the app needs to go get it from IMDB. Unfortunately, there doesn't seem to be an existing API to easily fetch the data (thank you Amazon - Amazon owns both AWS and IMDB). I could use other data sources, but that would be cheating. Therefore I decided to use Google in order to get the right link.   

**Step 3: scrape, scrape, scrape!**   
This is the part where the app scrape the HTML link in order to get the rating.   
   
All is left to do is to output the rating on the image and to show it to the user. 
