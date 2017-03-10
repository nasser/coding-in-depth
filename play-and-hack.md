# Session 1
## Play and Hack


### Play
Have students play the game for some time. Afterwards, ask them what they thought. Possible questions include:

- Was it fun?
- If so, how?
- If not, why?
- What would they change?

This does not need to be an in-depth game-literacy focused discussion, but deep enough to give the students concrete goals when they hack the game.

### Hack the game
Have your students tweak values, add and remove components so that the game plays differently without writing code. The challenge is to make a game that is as different as possible before any code is introduced. This stresses the importance and power of the GameObject/Component design of Unity. Ideally, this exercise will lead students to get excited by modifying the game, but frustrated at the limitations of value tweaking. This frustration speaks to the importance of writing code, without which you are beholden to modifying the work of others.

The components that make up the game are designed for this. Their names are descriptive and every field is commented with the role it plays. Familiarize yourself with the components before class so you can effectively guide the students in hacking the game.

A focused *prompt* or challenge is a good way to guide students in an otherwise open ended exercise. In addition to their ideas of what they would change about the game from earlier, possible prompts include:

- How can we make the game really hard?
- How can we make the game really easy?
- How can we make the game "better" ?

Work through the first prompt together. State the goal clearly, and tweak the values of the game to achieve it. Make sure to demonstrate

- Changing values on a component
- Adding a component
- Removing a component

at least once each. Follow the guidance of [type-along coding](type-along.md) (even though no code is being written yet).

Once everyone has that mod working, present them with another prompt, and let them tackle that on their own. Depending on available time, present them with more prompts or let them hack the game as they wish until the end of the session.

#### Suggested Hacks
* Disable the Player's Keyboard Forward Backward Mover Component to turn the game into a stationary turret shooter
* Replace the Player's Keyboard Forward Backward Mover Component with a Forward Mover Component to make a game where you can'd stop flying forward. Adjust the speed to 3 for an interesting balance!
* Drag the Bullet prefab on to the Clone variable of the Asteroids' Clone on Collision Component to make a game where Asteroids spawn a bullet when they're hit! Try adding more Asteroids to cause a chain reaction!
* Replace the Player's Keyboard Forward Backward Mover and Keyboard Rotater Components with a Follow Mouse Component to make a totally different kind of game. This one requires a keybaord *and* a mouse to control.
* Replace the Asteroids' Forward Mover Components with Follow Mouse Components to make a two player game where one player controls the ship with the keyboard and a second player controls the asteroids with the mouse! Use a low value of Closeness (e.g. 0.01) for best effect.
