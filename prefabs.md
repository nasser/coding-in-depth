# Session 4
## Prefabs

We're almost there! The last thing that's missing is the fact that the enemy is shooting the player's bullets. To fix this, we need to make a new *prefab* for the enemy's bullet and drag that into the `CloneOnTimer` Clone variable.

A [Prefab](https://docs.unity3d.com/Manual/Prefabs.html) is a collection of GameObjects, Components, and field values. They are useful for objects that need to be reused. The game already has prefabs for the player's bullet (called "Bullet"), the losing and winning text, and the three small asteroids that spawn when a larger asteroid is destroyed.


### Enemy Bullets
The enemy bullet is almost identical to the player's bullet, except:

1. It should look different
2. It should remove the player
3. It should move slower than the player's bullet

Make a copy of the Bullet prefab, rename it "Enemy Bullet", and give it the following component field values:

![](U42WlGyvnhHb8Ut9g7Uw.png)

These values are identical to the Bullet prefab except in the `SpriteRenderer`'s Sprite value, the `ForwardMover`'s speed value, and the `Destroy` scripts.

Drag the Enemy Bullet prefab on to the Clone variable of `CloneOnTimer` and the game is finished!

#### Exercise

* Experiment with different values for the Enemy Bullet's speed. What impact does it have on the game?
* Remove the `DestroySelfOnCollision` script that destroys Asteroids. What impact does this have on the game?
