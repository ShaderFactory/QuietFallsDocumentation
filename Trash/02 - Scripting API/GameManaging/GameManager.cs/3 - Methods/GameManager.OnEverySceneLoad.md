---
tags:
  - Method
---
```
private static void OnEverySceneLoad()
```
## Description
This method is triggered each time a new scene loads, making it ideal for implementing logic shared across all scene transitions. It is manually invoked once by [[GameManager.OnGameStart|GameManager.OnGameStart()]] and subsequently called by SceneManager (not yet implemented).
## Usage Example
```cs
using UnityEngine;

public class ExampleSceneManager : MonoBehaviour
{ 
	 private static void LoadNewScene(string sceneName)
        {
			//... New scene logic
			GameManager.OnEverySceneLoad();
        }
}
```