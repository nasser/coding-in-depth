# Session 4

<!-- `DestroySelfOnCollision` -->

```cs
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class DestroySelfOnCollision : MonoBehaviour
{
	public string with;

	void OnCollisionEnter2D(Collision2D collision)
	{
		if (collision.gameObject.tag == with)
		{
			Destroy(gameObject);
		}
	}
}
```


<!-- * [`OnCollisionEnter2D`](https://docs.unity3d.com/ScriptReference/MonoBehaviour.OnCollisionEnter2D.html)
* [`Destroy`](https://docs.unity3d.com/ScriptReference/Object.Destroy.html)
* [Tags](https://docs.unity3d.com/Manual/Tags.html) -->
