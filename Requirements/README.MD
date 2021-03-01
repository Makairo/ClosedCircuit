USER STORIES: <br>
As a player, I want a game that I can pick up at any time and play. <br>
As a player, I want a leaderboard where I can view other peoples scores and compare myself too. <br>
As a player, I want a game that I can stop / pause at any time and resume later.<br>
As a player, I want a game that I can play for as long / short as I want too.<br>

<br><br>
Given a new user, will be able to launch and start the game.<br>
Given a new user, will be able to access the leaderboard to view.<br>
Given a new user, will be able to create a username and login.<br>
Given an existing user, will be able to login and view saved progress.<br>
Given an existing user, will be able to start a new game or load an existing file.<br>
Given an existing user, will be able to view the leaderboard.<br>
Given an existing user, will be able to view all of their personal scores.<br>
Given an existing user, will be able to register a score on the leaderboard upon completing the game.<br>
Given any user, will be able to play the game until completion.<br>
Given any user, will be able to lose the game.<br>
<br><br>

UML (USE CASE DIAGRAM)
![UML DIAGRAM](Use-CaseDiagram.jpeg)
<br><br>

Requirement List:<br>
<br>
1. The system will prompt the user with the game screen upon loading.<br>
   - i. The user will have an option to login.<br>
        - a. If the user does not have a login, the user will be able to create one.<br>
        - b. If the user has a login, will have to option for the game to "remember" them.<br>
   - ii. The user will have an option to view the leaderboard.<br>
         - a. If logged in, the user can filter by their entries.<br>
         -b. If logged in or not, can filter list by user.<br>
   -iii. The user will have an option to start the game.<br>
         - a. User can place towers, and start waves manually.<br>
         - b. User can play to wave 50 and end, or go into endless mode.<br>
 - iv. Upon completing the game the game will prompt the user to upload their score.<br>
   - a. If logged in, user can choose to upload or not.<br>
   - b. If not logged in, the user can create a login and upload, or not.<br>
      <br>
2. The system will store each score in the database by user, and run game logic.<br>
 - i. Given score from user will upload to database with username, score, and date/time.<br>
 - ii. Given request by user, will display scoreboard to users.<br>
   - a. Can filter by self, or search username.<br>
 - iii. Game will perform game logic each round the user plays.<br>
   - a. Enemy pathing.<br>
   - b. Tower AI and logic.<br>
   - c. Game logic with rounds and a "Game Over" and "Game Complete" state.<br>
 - iv. Will store general round information in a database.<br>
   - a. Enemy spawns, wave presets, point amounts on wave completion.<br>
 <br>
3. The system will be developed with C#, SQL, and ASP.NET<br>
 - i. System will be hosted on Github, Azure, and have a client side application.<br>
   <br>
   <br>
