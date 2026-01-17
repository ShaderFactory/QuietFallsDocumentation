---
tags:
  - Property
---
```
public static GameManager instance;
```


## Description
Refers to the singleton instance of the GameManager class.
Publicly accessible, allows for the GameManager instance to be accessed from anywhere in the project.

## Usage Example
```cs
using UnityEngine;

public class ExampleClass : MonoBehaviour
{
	void Example()
	{
		[[GameManager.instance]].OnEverySceneLoad();
	}
}
```

