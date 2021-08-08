# Hacker News Scraper

The Hacker News Scraper is a Python terminal application that allows users to view posts from Y Combinator's Hacker News. Hacker News is a news site focusing on computer science and entrepreneurship. Users can see their desired amount of posts and post information from either the "trending" or "newest" pages of the website. 

This application runs in Code Institute's mock terminal on Heroku. 

## User Experience (UX)

### User Stories:

-   The user wants to access Hacker News stories via the terminal.
-   The user wants to be able to see trending stories.
-   The user wants to be able to see the newest stories.
-   The user wants to choose how many stories they want to see.
-   The user wants to see information on the stories, e.g. title, link and post age.
-   The user wants to be able to keep feeding through posts after the initial ones are displayed. 
-   The user's input should be validated at all stages.

[Logic Flowchart](<readme/HN Scraper Flowchart.png>)

## Features

### Existing Features

-   View trending posts.
    -   Users have the ability to view a stream of posts from the front page of Hacker News.
-   View newest posts.
    -   Users have the ability to view a stream of posts from the most recent posts page.
-   Post title.
    -   Users are shown the title of each post requested.
-   Post link.
    -   Users are shown the link to the article of each post. This link can be copied in the Code Institute terminal or clicked on in some other local terminals.
-   Post age.
    -   Users are shown how long ago the post was created.
-   Request certain amount of posts.
    -   Users have the ability to instruct how many posts they want to be printed to the terminal.
-   Request more from post stream.
    -   After the initially requested posts are shown, the user will be prompted to see if they want to view more posts from the given category (trending/newest), if there are any left.
-   Post count.
    -   The user is shown how many posts are available to be shown. There are a maximum of 30 for each of the two categories, due to this being the amount shown on a full page of Hacker News. This number will go down as the user requests more posts.

### Features to Implement in the Future

-   Option to sort posts by votes.
-   Unlimited post stream.
-   Display additional post data.

## Data Model

The model for this application consists of a Posts class. This class is instantiated with either the parsed HTML for the front page of Hacker News or the first page of newest posts.  

The get_info() method within this class is responsible for retrieving the post data from the parsed HTML. This method creates a dictionary for each post. Each dictionary stores the post title, link, and date posted. These dictionaries are then all stored in a single list that can be looped through to retrieve a requested amount of post data.

The Posts class also has additional methods that handle user requests for more posts and printing initially requested post data.