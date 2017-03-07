# Session 2

Students begin writing code to add an enemy to the game. For this session, we will add the enemy, and cause it to follow the player.

![](enemy.gif)

## Goals
- Understand the difference between C# and Unity
- Experience first exposure to code
- Make a digital enemy that follows the player around
- Understand basic linear algebra as its needed by games

## New Code

```cs
using UnityEngine;
using System.Collections;

public class AlwaysLookAt : MonoBehaviour {
  public GameObject target;

  void Update () {
    transform.up = target.transform.position - transform.position;
  }
}
```

<!-- * what is `using ...`
* what is `public class ...`
* what is `MonoBehaviour`
* what is `public GameObject target` + add comment?
* what is `void Update()`
* what is `transform`
* what is `transform.up`
* assignment
* vector math

![](vO3XwID5Cpg92XO55VuRg.png) -->
