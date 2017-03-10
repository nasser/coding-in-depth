# Session 1
## How Unity Works

Unity is designed around a particular set of ideas meant to make your work as a game developer easier. Understanding these ideas is crucial to using Unity effectively, and working contrary to them will cause a lot of undue headache.

### Games In General

The core idea behind Unity is that most games are full of "things" that interact with each other and react to player actions in different ways over time. For example, some of the "things" in Asteroids are the player's ship, the asteroids, and the player's bullets. The way they interact with eachother is different for each "thing" and might depend on events are happening in the game. For example, when a bullet touches an asteroid, the asteroid disappears, and is replaced with three smaller asteroids. When the player presses the right arrow key, the ship turns right. Most games can be described by different "things" and how they interact.

![](http://static1.gamespot.com/uploads/original/1539/15391776/2583507-5676190985-aster.png)

#### Exercise {#exercise-identify-things}
Have the class identify "things" and interactions in other games, and suggest your own.

### Unity In Particular

Unity calls these "things" [GameObjects](https://docs.unity3d.com/Manual/GameObjects.html). *Everything* in your game is a GameObject. Players, enemies, pickups, parts of levels. Even things that are not immediately visible are GameObjects, like the area that marks the finish line in a racing game or the starting point in a platformer.

GameObjects on their own do not do anything, and they are all equal. There is not, for example, a camera GameObject and a spaceship GameObject, just GameObjects. They are blank, empty containers waiting to be filled with the logic and behavior that comes from [Components](https://docs.unity3d.com/Manual/Components.html). A Component is a chunk of code designed to do one specific thing when attached to a GameObject. Some common Components are built in to Unity. These include the [Camera](https://docs.unity3d.com/Manual/class-Camera.html) Component that draws the scene on the screen, the [Rigidbody](https://docs.unity3d.com/Manual/class-Rigidbody.html) Component that makes GameObjects move with realistic physics, or the [AudioSource](https://docs.unity3d.com/Manual/class-AudioSource.html) Component that plays sound files. You will not have to recreate these for every game. But more game-specific logic, like the way the player moves, or how pickups work, will need to be specified by the game developer by writing code.

So, GameObjects *contain* Components, and Components must be *attached* to GameObjects. Unity’s core idea is: everything in your game is a GameObject, and you tell GameObjects how to act and how to look by attaching Components to them.

![](https://d2mxuefqeaa7sj.cloudfront.net/s_02986F66D20964F9BB6F25081A8646F27F4CE29D977FD708E3973173FB7632C8_1487449484328_file.png)

As an example, the player's ship in Asteroids could be a GameObject with:

- A component specifying what image to use to draw the ship
- A component specifying its position and rotation
- A component that creates a bullet GameObject when the player presses a button
- A component that rotates the ship when the player presses left or right
- A component that moves the ship forward the player presses forward or backwards
- A component that removes the ship when it touches an Asteroid

That's a lot of components! This is how Unity wants you to build your games, though. The idea is that if you write small, generic components that aren't tied to one particular GameObject, you can re-use them on other GameObjects.

Once you're thinking in terms of GameObjects and Components, you're ready to take on Unity!

The way you organize your game, the number of Components and what goes in them is up to the developers. Every team finds a style that works for it, and it is not an exact science. For example, in the earlier Asteroids player ship example, the movement and rotation Component could be combined into one. This would not be "wrong" and breaking them apart is not necessarily "better". Stress with your class that there is always more than one way to solve a problem, and part of the challenge of computer programming is finding an approach that works for everyone involved.

#### Exercise {#exercise-break-down}
Ask the class to try and break down popular "things" in video games into Unity-style Components. Ask the students what games they play and what "things" they contain that can be broken down, and suggest your own. Guide them towards thinking of common, reusable Components between "things".

If Mario was made in Unity, there would be no “mario” object, just a normal GameObject named Mario with a Component that says what he looks like, a Component that says how he should move, a Component that says how he can get hurt, and so on.

### Take Aways

* Unity organizes games into GameObjects and Components
* GameObjects organize all the "things" in your game and contain Components
* Components implement behavior and logic, and only exist attached to GameObjects
* Components are either built into Unity or are programmed by you
* The only way to write code in Unity is to make new components and attach them to GameObjects
