---
tags:
  - Property
---
```
private List<GameManagerBase> gameManagerList;
```
## Description
List of all Game Managers in the game. This is used to initialize them in order.

## Usage Example
```cs
using UnityEngine;

public class ExampleClass : MonoBehaviour
{
	void Example()
	{
		GameManager.instance.gameManagerList.Add(new GameStateManager());
	}
}
```