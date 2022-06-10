# Webackend-Project-3
Tracking the Statistics

Developing RESTful back-end microservice and run multiple instances of the new service with load-balancing and sharding.

The following are the learning goals for this project:

1.Gaining further experience with implementing back-end APIs in Python and FastAPI.

2.Running and debugging multiple instances of a web service process.

3.Implementing application-level sharding for a relational database.

4.Configuring and testing an HTTP reverse proxy and load balancer.

Adding a New Service

Create a RESTful microservice for tracking user wins and losses. Your service should expose the following operations:
Posting a win or loss for a particular game, along with a timestamp and number of guesses.


Retrieving the statistics for a user. If you visit Wordle, open your browser’s developer tools, and examine local storage for the entry nyt-wordle-statistics, you’ll see that it uses the following format, which your service should also return:

{
   "currentStreak": 4,
   "maxStreak": 5,
   "guesses":{
      "1": 0,
      "2": 0,
      "3": 2,
      "4": 3,
      "5": 4,
      "6": 2,
      "fail": 1
   },
   "winPercentage": 92,
   "gamesPlayed": 12,
   "gamesWon": 11,
   "averageGuesses": 5
}

Note: the names "1" through "6" are not valid identifiers for class members in Python, so if you are returning a Pydantic model as a response you will need to use Field customization to set an alias for each of these.

Retrieving the top 10 users by number of wins

Retrieving the top 10 users by longest streak


