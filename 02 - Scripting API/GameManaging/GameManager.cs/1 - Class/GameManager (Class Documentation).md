---
tags:
  - Class
Asset Type: C# Script
---
## Description
This script is contains the initialization procedure of the game. It is responsible for instantiating the GameManager MonoBehaviour (GameObject) in the scene.

Although derived from MonoBehaviour, this script is neither required nor intended to be present in the scene. It is able execute code to create its own GameObject, attach itself to it, and then instantiate all other GameManager instances.
## Properties

| Property                                         | Description                               |
| ------------------------------------------------ | ----------------------------------------- |
| [[GameManager.instance\|instance]]               | Singleton instance of GameManager         |
| [[GameManager.gameManagerList\|gameManagerList]] | List containing all of the game managers. |

## Private Methods
| Method                                             | Description                                                              |
| -------------------------------------------------- | ------------------------------------------------------------------------ |
| [[GameManager.OnGameStart\|OnGameStart]]           | The very first method called in the game code. Performs initial set ups. |
| [[GameManager.OnEverySceneLoad\|OnEverySceneLoad]] | This method is called every time a new scene is loaded.                  |


## Current Code (Subject to change)
Link to the #CodeFile : [[GameManager.cs (Code)]]
