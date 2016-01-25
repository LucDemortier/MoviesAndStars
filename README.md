# MoviesAndStars
Project Luther for Spring 2015 Metis Data Science Bootcamp.
See blog post at [lucdemortier.github.io](http://lucdemortier.github.io/portfolio/2_luther.html) for a description of the results.

iPython notebooks used to generate the results and plots for the MoviesAndStars project:

1. **MovieScrape**: 
  - Scrapes BoxOfficeMojo website for info about all movies released during a given year.
  - Stores the result in a pickle file of the form XXXX_all_movie_dict.pkl, where XXXX is the year.
2. **OscarScrape**: 
  - Scrapes the Oscars webpages and collects all nominations and wins in categories containing the keywords "Actor", "Actress", and "Directing" from 1950 until 2015. 
  - Stores the result in pickle file oscars.pkl. 
  - Corrects various mistakes and stores the result in oscars_c1.pkl.
  - Creates a dictionary keyed by Actor/Actress/Director name, and with values equal to [no. of nominations, no. of wins].
  - Stores the result in aad_oscars.pkl.
3. **AnalyzeThis**:
  - Reads in the pickle files created by MovieScrape and OscarScrape and creates a dictionary of movie features, including the star value of a movie's cast, which is defined as the total number of oscar wins and nominations by actors, actresses, and director of the movie, won in years previous to the movie's release.
  - Turns above dictionary into a Pandas dataframe for further processing.
  - Generates all the plots shown on the blog, and a few more.
  - Performs a quantile regression of Total Domestic Revenue versus Star Value of Cast.
  - Performs an ordinary linear regression of Total Domestic Revenue versus Production Budget.

In addition to these iPython notebooks, the repository also contains a short document, BrainStorming.pdf, with the results of a brainstorming session done at the beginning of this project with a few colleagues.
