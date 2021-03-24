# ClosedCircuit
**Personal Game Project for MSSA SD9**<br>
**______________________________________________________________________________________________________________________________________________________**<br>
**Table of Contents:** <br>
________________________________________________________________________________________________________________________________________________
1. [Requirements](https://github.com/Makairo/ClosedCircuit/tree/main/Requirements) <br>
2. [Prototype](https://github.com/Makairo/ClosedCircuit/tree/main/Prototype) <br>
3. Description and Project Plan (below) <br>
________________________________________________________________________________________________________________________________________________

I aim to create a single player top-down strategy tower defense game. In essence the player would choose a map to play on, and there will
be a pathway going from the left side of the screen to the right. Enemies of varying strength, health, and speed would follow the pathway laid out, and if they 
made it off the screen on the right, the player would lose lives. The player would start with 100 lives, and each life an enemy has when they reach the 
other side would subtract from the total. There would be 4 types of enemies: The first being a slow, 1 hp mob that suits a fodder role. The second would have 20hp, 
but move slightly slower. The third would be an extremely fast enemy but only have 5hp. The last option be be sort of a boss mob, 50hp but move extremely slowly.
The goal for the player is to create towers along the pathway (but not on it directly) that will damage the enemies running the pathway. There would be 4 types 
of towers: The first being a cheap, well-rounded tower that damages one enemy at a time. The second be a more expensive option that deals damage to enemies in
an area of effect. The third would be crowd control option, a tower that doesnt deal damage but instead slows enemies down. Lastly, the forth option would be an
extremely expensive option but in essence be a combination of all the towers listed prior. Enemies spawn in waves, giving the player some breathing room between
to place and reposition towers. Every enemy defeated gives 1 point, and every wave defeated will give 100 times the round number in points. Points are used to
purchase towers. To complete the game, the player would have to complete a predetermined wave and upon completion of it, the game would end.

SOFTWARE CONCEPTS AND IMPLEMENTATION

The software in my concept would have to manage a user interface, count lives and recognize a "game end/over", deal with tower and enemy AI, establish the pathway on 
a given map for the enemies to traverse, and allow the player to place towers on the grid. The user interface would display lives and the number of points 
currently owned. A simple int or double counter would sufficefor both. A game over would end the current map and send the user back to the main menu with a 
"You died!" message. This can all be done in 1 or 2 methods and have it print it to the screen. The difficulty would lie in the enemy and tower AI. Enemies 
would have to move at varying speeds, have a health bar and be able to be interacted with by the towers. Each enemy could be defined in their own class, so that 
their methods do not overlap one another. Variables would have to be used to store and modify the movement speed and health of each enemy. There would have to 
be a "creation" method for every instance of an enemy, since each one is a seperate entity.	The towers would have to have a range, a targeting algorithm to choose 
which enemy to attack out of the ones that are in range, a damage value to deal to targets, and be able to be placed and moved by the player. Each tower could 
again be defined in their own namespace, to avoid confliction, and a creation method, since each tower is a seperate entity. Towers would have to have a creation,
deal damage, and deletion method at the very least.

The calculation for dealing damage to an enemy would be called hundreds of times per instance of the game, so creating a simple and efficient method to perform
the calculation is critical. It would be passed the enemy health, and the damage dealt, and then return the value back to the entity that called it. The entity itself
would be concerned if that damage was fatal and then delete itself from there. In total there would be a creation, move, takeDamage, and deletion method for each
enemy that spawned in. 

The map itself would have to be defined in 2 regions, the "pathway" and the "player field". The pathway would be a one way path, with a few curves here and there, 
for the enemy to follow. The enemies would move down the direction of the pathway to the end of the screen, where they would deduct lives and despawn. The 
player field would be the rest of the area on the map that allows for the player to place down towers. The user interface would also have to have a tower 
purchasing interface, deducting points for towers purchased and allowing the player to place them where they wanted.

The input from the user that the game takes would be the start of each map, the placement of the towers, and other menu interfaces. Aside from that, the game
creates it own inputs. The enemies and towers interact with each other, the map and the towers, and the map and enemies will interact with each other. The result 
from this end in a visual display of the enemies progressing from one side to the other, being damaged by towers and dying. Points accumulate and waves increase. 
If you ever run out of lives, then the "game over" screen will flash and it's up to the player to reset it and try again. The desired end game is to defeat all
the waves to the predetermined wave, at which point the game will be won and the application end.

EXTERNAL RESOURCES / INSPIRATIONS

Tower defence games are not uncommon, which is difficult when it comes to marketing a new IP and getting it out there, but also gives plenty to reference and
take inspiration from. Games that I've taken reference from, and will most likely look to for solutions to issues when designing certain aspects, include: "Bloons
Tower Defence" by Kongregate, "Kingdom Rush" by Ironhide Game Studio, "Plants vs Zombies" by PopCap Games, and "Orcs Must Die! 2" by Robot Entertainment. They all 
deal with different aspects of gameplay in their own unique ways, and I feel that ignoring their approaches would be criminal. In addition, the user ATBrackeys 
on Github has a unity tutorial on creating a tower defence game, which is also published to youtube.com. He takes an interesting approach to defining the 
pathway on the map, by using nodes that the enemies travel to in sequence to the end. This game will be written in C#, so the most that can be taken from this 
is conceptual assistance and solutions, but that is still welcome.

PROJECT PLAN

My current plans going forward is to first create an interface and create a map. This would include variables like health and points, a game over screen, 
a menu, and a simple map to start off. The second step I'll take is to create the first enemy, and ensure that their health, speed, and creation work properly.
After that will be to implement the first towers into the game, and design their targetting AI; that they deal damage and otherwise act as intended. 
After all the core mechanics are implemented, adding the other variants to the enemies, towers, and maps will be up next. From there, fine tuning and bug testing 
will occur and the mechanics and engine will be polished. If time allows and the game is complete, more enemy variants, tower variants, or maps can be added and 
beef the content out. A great thing about this genre of game is that adding content is very simple, as the format gives you near infinite possibilites of towers,
enemies, and maps that you could create and expand upon.

I couldn't be more excited to start this development process in SD9. It's an opportunity to test my potential and experience, even if in a small capacity,
the process for creating and developing software and applications. Even if some things fail, there is alot to be gained from knowledge and experience with this.
I chose a game, as it's a big hobby of mine, and even simple concepts can escalate decently quickly into complexity. I wanted something that had challenge to it, 
but reasonable for the timeframe and experience that we have to complete and in a capacity that I'll be proud of. I hope that you will enjoy my end result.
