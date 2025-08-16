---
tags:
  - Manual
---
This document goes over how the game managers are set up, what systems are instantiated, which GameObjects are spawned in the scene and how they work together.

### How should you set up the scene for proper initialization?
You do no need to worry about this! As discussed in the [[Philosophical approach to the game architecture]], the game should automatically spawn the Game Managers in the scene and make them scene persistent.

### What happens when you start the game.
1. When the game starts executing, the [[GameManager (Class Documentation)|GameManager.cs]] script, even though not present as a component in any GameObject, will execute the necessary code to spawn the Game Managers in the scene and will execute the Unity's [DontDestroyOnLoad (Object target)](https://docs.unity3d.com/ScriptReference/Object.DontDestroyOnLoad.html) so the managers are scene persistent.
   It then calls the respective Initialize() methods for each single one of them, allowing each manager to execute their own Initialization logic if needed. The reason to execute the Initialize() method instead of using Monobehaviour's Start for example, is to control the execution order. 

