---
tags:
  - Method
---

```
 [RuntimeInitializeOnLoadMethod(RuntimeInitializeLoadType.BeforeSceneLoad)]
 private static void OnGameStart();
```
## Description
It is the very first method called in the game code,responsible for calling other methods to initialize the game setup.

The ==[RuntimeInitializeOnLoadMethod(RuntimeInitializeLoadType.BeforeSceneLoad)]== attribute ensures the code executes automatically, even though the GameManager script is not attached to a GameObject in the scene.

## Usage Example
```cs
using UnityEngine;

public class MyGameManager : MonoBehaviour
{ 
	[RuntimeInitializeOnLoadMethod(RuntimeInitializeLoadType.BeforeSceneLoad)]
	 private static void OnGameStart()
    {
		ExampleSetUpGameManagers();
		ExampleSpawnPlayer();
	}
}
```