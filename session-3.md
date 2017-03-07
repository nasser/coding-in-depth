# Session 3

Students make the Enemy respond to collision with the player's bullets by disappearing.

![](destroy-self.gif)


## Goals
* Begin to understand Unity's physics engine
* Make multiple components work together

## New Code

```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class DestroySelfOnCollision : MonoBehaviour
{
	public string otherTag;

	void OnCollisionEnter2D(Collision2D collision)
	{
		if (collision.gameObject.tag == otherTag)
		{
			Destroy(gameObject);
		}
	}
}
```

<!--
* similarities
 [`OnCollisionEnter2D`](https://docs.unity3d.com/ScriptReference/MonoBehaviour.OnCollisionEnter2D.html)
* [`Destroy`](https://docs.unity3d.com/ScriptReference/Object.Destroy.html)
* [Tags](https://docs.unity3d.com/Manual/Tags.html) -->
