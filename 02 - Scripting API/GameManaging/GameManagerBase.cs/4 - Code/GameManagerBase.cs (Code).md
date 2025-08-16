---
tags:
  - CodeFile
---
## Information
| Last Updated  | August 12th 2025                          |
| ------------- | ----------------------------------------- |
| Documentation | [[GameManagerBase (Class Documentation)]] |

```cs
using UnityEngine;

/// <summary>
/// Base class for all game managers. Making all of the classes inherit from this class allows for all 
/// game managers to be spawned, initialized and managed in a consistent way.
/// </summary>
public abstract class GameManagerBase : MonoBehaviour
{
    public bool isInitialized = false;

    #region Abstract Methods
    public abstract void Initialize();
    #endregion

    public static GameManagerBase InstantiateUnderContainer(GameManagerBase managerType)
    {
        GameObject go = new GameObject(managerType.GetType().Name);
        return go.AddComponent<GameManagerBase>();
    }

}

```