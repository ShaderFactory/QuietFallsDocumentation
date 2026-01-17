---
tags:
  - Manual
---
## The game should not rely on scene GameObjects to work!
Games that require scenes to include a GameObject with attached scripts can become cluttered, and the risk of the game breaking due to a missing GameObject is frustrating. To address this, the [[GameManager (Class Documentation)|GameManager]] executes initialization code without requiring any GameObject with scripts attached, ensuring all systems function as intended.

