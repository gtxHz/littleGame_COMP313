# What is the main action in the game?

The main goal of this game is to control the ball, collect all the crystals and reach the final destination.
When reaching the finish line, the shorter the player takes, the higher the final score will be.
Players can control the movement of the ball by pressing the *W S A D* to move back,forth,left and right. 

The ball is affected by physical factors such as friction and inertia, so players need to try for a while before they can fully adapt to the movement of the ball.
The player needs to collect all the crystals to reach the end to trigger the victory condition, and the UI will always show the player's time spent,
the number of crystals collected so far and the total number of crystals in the level.

Also,in the UI interface, players can also adjust the sound level and graphic quality



# What was the hardest part of the game to get working in Unreal?

When working with the UE4 engine, I thought that as a beginner, I could only learn new areas better by starting with the basics. 
I decided not to use any existing templates or take existing plugins and blueprints from the UE Mall. Therefore, this made it a lot more difficult for me to develop the game.

At the beginning, I found that controlling the movement of the ball is not quite the same as controlling the movement of the character. 
The ball has physical properties, it is the force that makes it move, so our input should be a constant input force for it. 
It wasn't until I found torque, a physical property, that I was able to solve the problem of moving the ball very well.

The second, more difficult part is dealing with the individual variables in the game, and the logic of how the game runs. 
I found that GameInstance acts like a global repository that stores individual variables and calls this repository when other blueprints handle the logic.

And I think the most difficult part when working with UE4 is the sound control in the UI list. 
The function binding slider is easy to handle, but how do I get the current floating point value from the callback function that binds the slider to the sound blueprint?
Then I found the solution. Reference the sound blueprint in the UI file, then get the value of the sound in the object of the sound blueprint, and slide the slider to assign this value to the value represented by the current slider. 
After that, call the ChangeVolume function defined in the sound blueprint. This function takes the sound file in the blueprint and executes the set volume mutiple function.
Finally the value of the slider is passed to the set Volume mutiple function of the blueprint sound file.


# What is the most interesting part of the game?

I remember in my childhood I played a video game called Hamster Ball. 
In this game, you need to control the hamster ball to avoid all the obstacles and reach the final destination within the specified time, which gives me a lot of fun.
I think adventure and collecting is the fun part of this type of game (ball movement game).
Players in such games seek to complete the level in the shortest possible time.
Players break through themselves again and again, and this is the most fun of the game.