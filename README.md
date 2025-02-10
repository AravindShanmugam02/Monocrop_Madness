# Monocrop Madness
## About Game
An educational game built around the theme of farming simulation for dissertation project. This game attempts to educate the harmful effects of monocropping and gives the player an idea of how to avoid it through gameplay. Built with Unity3D using c#.
### Technical Details
#### 3Cs
***Camera, Character, Control***<br/>
[Place Holder for video]<br/>
Basic player character movement and camera movement.<br/>
<details>
 <summary>Code Snippet</summary>
</details>

#### AI
***AI Character***<br/>
[Place Holder for video]<br/>
AI was implemented as a <ins>HFSM</ins> (Hierarchical Finite State Machine).<br/>
[Place Holder for AI states diagram overview]
<details>
 <summary>Code Snippet</summary>
</details>

[Place Holder for video]<br/>
AI has a <ins>FOV</ins> implemented to detect player during patrol state.<br/>
<details>
 <summary>Code Snippet</summary>
</details>

#### UI
***Crosshair***<br/>
[Place Holder for video]<br/>
Can interact with objects in the world using crosshair. The interaction options that were displayed to player varies from object to object. A <ins>Ray</ins> is casted from camera through the crosshair in UI to detect what game world objects player is interacting with.<br/>
<details>
 <summary>Code Snippet</summary>
</details>

***Tip***<br/>
[Place Holder for video]<br/>
Tips, hints and pop-ups are constructed by this system. Based on the system that triggers a pop-up, the urgency is validated and the urgent messages are poped on the screen for player within 0.5 seconds.<br/>
<details>
 <summary>Code Snippet</summary>
</details>

#### Core Mechanics
***Inventory***<br/>
[Place Holder for video]<br/>
A click-based-interaction inventory was implemented. Has interactions such as:<br/>
* <ins>Swap</ins> (Equiped slot to inventory slot and vise versa.)
* <ins>Stack</ins> (Stack same items in equiped slot from inventory slot and vise versa. Has a stack limit.)
* <ins>Drop</ins> (Drop equiped items. Can only drop an equiped item.)
* <ins>Move</ins> (Move items from equiped slot to inventory slot and vise versa. But <ins>cannot drag items</ins> because inventory was implemented to have click interactions.)
<details>
 <summary>Code Snippet</summary>
</details>

***Timer***<br/>
[Place Holder for video]<br/>
A timer was implemented that controls <ins>game time</ins>, <ins>day & night cycle</ins>, in-game day-to-day <ins>weather</ins> (weather, climate, temperature), <ins>calender</ins>, and also has many useful <ins>time conversions</ins>. The temperature and weather for the following day in game were given random values at the end of each day cycle using a <ins>seed</ins> of type <ins>System.Random</ins>.<br/>
<details>
 <summary>Code Snippet</summary>
</details>

***Farm***<br/>
[Place Holder for video]<br/>
The mechanic that delivers educational content through gameplay. Both AI and player can do farming. Farming has many sub-actions such as:
* Cropping
   * <ins>Till</ins> (Plough the land.)
 * Water (Water the land.)
   * <ins>Cultivate</ins> (Plant seeds.)
* Harvesting
   * <ins>Harvest</ins> (Harvest the yields after the crops are grown up.)
* Fix Monocropping
   * <ins>Destroy</ins> (Destroy cultivated crops on selected land. This step is needed to restore the land affected by monocropping practice.)
   * <ins>Restore</ins> (Restore the land affected by monocropping practice.)
Certain actions need some specific tool to complete them.<br/>
<details>
 <summary>Code Snippet</summary>
</details>

[Place Holder for video]<br/>
Farming system also has other mechanisms that are incorporated to work together such as:
* <ins>Cropping pattern tracking system</ins> (Keeps track of what the player had planted last 3 times. Detects the overall pattern of the plot.)
* <ins>Farm land health system</ins> (Player should practice good farming methods to keep the farm land's health up so that plants grow well.)
* <ins>Crop growth system</ins> (Is affected by weather and how the player maintains the farm land.)
* <ins>Farming feedback system</ins> (Happens at the end of the day.)
* <ins>Community & Population system</ins> (Tied up with gameplay, so player won't have exclusive access.)
* <ins>Credit & Shop system</ins> (Used for buying seeds, food and farming tools.)

***Save, Load & Delete***<br/>
[Place Holder for video]<br/>
Save, load and delete game data. Uses binary formatter to serialise and deserialise data and saves to a file. Save is automatic and only happens when player completes slot1 in the game.<br/>
<details>
 <summary>Code Snippet</summary>
</details>

### Areas of Improvements
* Tip and pop-ups.
* Guiding player through how to farm and what are the rules through gameplay.
* The history and game plot can be said in a better way.
* Opening and closing of inventory and shops can be both by keyboard mapping and HUD button clicks.
* Restoring the land can erase all of it's cropping history, so that the gameplay is balanced.
* Community, population, credit and seeds storage can have better gameplay design balancing.
* Length of the game can be reduced & balanced.
* Educational content can be delivered in a more effective way.

## My Role
Unity Game Developer
### Tags
C#, Unity3D, Gameplay, AI, Interfaces, scriptable objects, Observer pattern, Singleton pattern
