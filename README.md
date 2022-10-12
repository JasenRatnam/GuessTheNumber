# guess-the-number-JasenRatnam
An application where user guesses a number and is told the exact and partial digit matches.
The user wins once the number is guessed with an exact match.

Using
* Spring Boot REST application 
* JDBC Template to access the database.

# REST endpoints:

* "begin" 
  * POST
  * Starts a game, Generates an answer, Sets the correct status. 
  * Return a 201 CREATED message and the created gameId.
* "guess" 
  * POST
  * Makes a guess by passing the guess and gameId in as JSON. 
  * Calculate the results of the guess 
  * Mark the game finished if the guess is correct. 
  * turns the Round object with the results filled in.
* "game" 
  * GET 
  * Returns a list of all games. 
  * in-progress games do not display their answer.
* "game/{gameId}" 
  * GET
  * Returns a specific game based on ID. 
  * in-progress games do not display their answer.
* "rounds/{gameId} 
  * GET
  * Returns a list of rounds for the specified game sorted by time.

# Rough ER Diagram

![ER diagram](ERD.jpg)
