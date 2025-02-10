# Monocrop Madness
## About Game
An educational game built around the theme of farming simulation for dissertation project. This game attempts to educate the harmful effects of monocropping and gives the player an idea of how to avoid it through gameplay. Built with Unity3D using c#.
## Technical Details
### Core Mechanics
***Inventory***<br/>
A click-based-interaction inventory was implemented. Has interactions such as:<br/>
* <ins>Swap</ins> (Equiped slot to inventory slot and vise versa.)
* <ins>Stack</ins> (Stack same items in equiped slot from inventory slot and vise versa. Has a stack limit.)
* <ins>Drop</ins> (Drop equiped items. Can only drop an equiped item.)
* <ins>Move</ins> (Move items from equiped slot to inventory slot and vise versa. But <ins>cannot drag items</ins> because inventory was implemented to have click interactions.)
<details>
 <summary>Video</summary>

https://github.com/user-attachments/assets/fde1b69c-0f01-4aa2-a03a-9fceb72291c5

https://github.com/user-attachments/assets/35eccb48-87fe-4b8f-a0e3-fc161c23cf53

https://github.com/user-attachments/assets/0ff171cd-cf07-4c18-aaae-f79c17ce8eb7

https://github.com/user-attachments/assets/49fce556-be52-472a-8a86-4fd7e89dbdcd

https://github.com/user-attachments/assets/c4d2cce8-8d93-4353-8e2d-c01f1ed96526

</details>
<details>
 <summary>Code Snippet</summary>
</details>

***Timer***<br/>
A timer was implemented that controls <ins>game time</ins>, <ins>day & night cycle</ins>, in-game day-to-day <ins>weather</ins> (weather, climate, temperature), <ins>calender</ins>, and also has many useful <ins>time conversions</ins>. The temperature and weather for the following day in game were given random values at the end of each day cycle using a <ins>seed</ins> of type <ins>System.Random</ins>.<br/>
<details>
 <summary>Video</summary>

https://github.com/user-attachments/assets/d12f9107-0521-410b-a5e6-a8af8290842d

https://github.com/user-attachments/assets/2fdbb145-54c6-4d16-8779-54febad9507e

https://github.com/user-attachments/assets/bfb7dca8-b91d-45c8-a6ce-acb86108aabe

</details>
<details>
 <summary>Code Snippet</summary>
</details>

***Farm***<br/>
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
 <summary>Video</summary>

https://github.com/user-attachments/assets/514294c8-e762-4a07-8b82-107087776df4

https://github.com/user-attachments/assets/6f722481-5669-4efa-b6ab-f9d2a30939ee

</details>
<details>
 <summary>Code Snippet</summary>
</details>

Farming system also has other mechanisms that are incorporated to work together such as:
* <ins>Cropping pattern tracking system</ins> (Keeps track of what the player had planted last 3 times. Detects the overall pattern of the plot.)
* <ins>Farm land health system</ins> (Player should practice good farming methods to keep the farm land's health up so that plants grow well.)
* <ins>Crop growth system</ins> (Is affected by weather and how the player maintains the farm land.)
* <ins>Farming feedback system</ins> (Happens at the end of the day.)
* <ins>Community & Population system</ins> (Tied up with gameplay, so player won't have exclusive access.)
* <ins>Credit & Shop system</ins> (Used for buying seeds, food and farming tools.)
* <ins>Barn system</ins> (Used for storing food from which your community will consume food at the end of every day.)
<details>
 <summary>Video</summary>

https://github.com/user-attachments/assets/d99b130b-8a23-4772-ab3b-d12082000e59

https://github.com/user-attachments/assets/bc3c762e-14b0-4c06-85db-6a16d6fd71f5

</details>

***Save, Load & Delete***<br/>
Save, load and delete game data. Uses binary formatter to serialise and deserialise data and saves to a file. Save is automatic and only happens when player completes slot1 in the game.<br/>
[Place Holder for video]<br/>
<details>
 <summary>Code Snippet</summary>
</details>

### AI
***AI Character***<br/>
AI was implemented as a <ins>HFSM</ins> (Hierarchical Finite State Machine).<br/>
[Place Holder for AI states diagram overview]
<details>
 <summary>Video</summary>

https://github.com/user-attachments/assets/7f6464f4-d531-41f6-aff9-aae7bf0e809a

https://github.com/user-attachments/assets/e264a402-f5df-4e65-9401-b9f394eff545

</details>
<details>
 <summary>Code Snippet</summary>
</details>

AI has a <ins>FOV</ins> implemented to detect player during patrol state.<br/>
<details>
 <summary>Video</summary>

https://github.com/user-attachments/assets/035cb7a3-e88a-4183-bbc9-72e8e47237b4

</details>
<details>
 <summary>Code Snippet</summary>
</details>

### UI
***Crosshair***<br/>
Can interact with objects in the world using crosshair. The interaction options that were displayed to player varies from object to object. A <ins>Ray</ins> is casted from camera through the crosshair in UI to detect what game world objects player is interacting with.<br/>
[Place Holder for video]<br/>
<details>
 <summary>Code Snippet</summary>
</details>

***Tip***<br/>
Tips, hints and pop-ups are constructed by this system. Based on the system that triggers a pop-up, the urgency is validated and the urgent messages are poped on the screen for player within 0.5 seconds.<br/>
[Place Holder for video]<br/>
<details>
 <summary>Code Snippet</summary>
</details>

### 3Cs
***Camera, Character, Control***<br/>
Basic character, camera movement and control.<br/>
<details>
 <summary>Video</summary>

https://github.com/user-attachments/assets/c4c91497-366c-4046-ae9e-641f6ae1d884

</details>
<details>
 <summary>Code Snippet</summary>
</details>

## Areas of Improvements
* Tip and pop-ups can be improved to have better appearance like in the side or corner.
* Guiding player through how to farm and what are the rules through gameplay.
* The history and game plot can be said in a better way.
* Opening and closing of inventory and shops can be both by keyboard mapping and HUD button clicks.
* Restoring the land can erase all of it's cropping history, so that the gameplay is balanced.
* Community, population, credit and seeds storage can have better gameplay design balancing.
* Length of the game can be reduced & balanced.
* Educational content can be delivered in a more effective way.

## My Role
Unity Game Developer
## Tags
C#, Unity3D, Gameplay, AI, Interfaces, scriptable objects, Observer pattern, Singleton pattern
