One of the most important design philosophies of Quiet Falls is the idea of building the project with modular—self-contained Unity Packages—Systems. The systems are not responsible for managing the flow of the game, or tell other systems what to do, they should only receive orders.

## How things worked before
Before coming to the realization that I should make Systems, not Games, I did not distinguish the differences between Game Managers and Game Systems. Even ending up using those terms interchangeably as I created my scripts inside the main Unity project.

## This is when I knew something was wrong.
One day, I needed to export the player character to test it in another Unity Project, and that was enough to make me question my life choices.


First, you select the character, and then you click "export", next you need to select all the dependencies. At that point, you realize that the character script references multiple systems within the main project.

The nightmare starts, you instantly start questioning your life choices. Your main player script references a camera script, that is part of a set of scripts that make up for your camera system.
You say: "Okay, I will just head back to the main project, and copy that script over". You do that, click inside the editor and let it recompile. But when it does, Unity realizes after compiling that newly brought in script, that that script that was missing, actually references 2 or 3 other scripts from the camera system and one more script from your navigation system as well!

Now imagine that it wasn't just that camera script that was initially missing, but a handful or possibly dozens of scripts!

By that time, I had already given a good amount of thought about what is a manager and what is a system. But it was in that day I realized the solution was to make modular, self contained systems.

## Not being self-contained cause other problems too
Even though this struggle with overdependency was what made me realize there was a problem, that is not even the worst problem.

When you don't isolate their functionality, things need to be build in order. But when you are making isolated—self-contained systems, you can pause working in parts you're tired or looking at or bored by , to go ahead to work on parts that you are excited about. Maintaining the enjoyment of making the game, which might be the most important thing for making sure the game finishes.

## Systems must be unaware of their surroundings
Systems don't need to care about the game flow, what happened before or what is going to happen after they do something. That's too much.

The problem of over dependence is not only the... [writing in progress]