# Overview
CE318 assignment consisting of designing and implementing a 3D game in Unity3D.
Simple 2 level FPS with the feel of old arcade shooters. Implemented with the [Unity FPS Microgame](https://assetstore.unity.com/packages/templates/unity-learn-fps-microgame-urp-156015) asset as foundation.

## Where can you play it?

[Play online in your browser](https://play.unity.com/en/games/d3a67b14-6d99-4226-b830-3ed4d8612a96/webgl-builds) - deployed to WebGL

# Galactic Fury

![image](https://github.com/user-attachments/assets/4848b737-e0c2-44e4-b01e-e369b0529ba0)


"Galactic Fury" is a high-octane first-person shooter set in a dystopian future, drawing inspiration from classic arcade games like "Doom" and "Unreal Tournament." Players embark on a mission to confront a rogue AI, Anton, which controls Echelon, a militaristic outpost filled with AI-controlled robots. The game unfolds on a distant alien world, featuring a rocky terrain with lava rivers orbiting a Saturn-like planet. Players, assuming the role of David Bowman, a top space marine and the sole human survivor on Echelon, face intense combat against waves of robotic enemies. The gameplay emphasizes fast aiming, agile movement, and strategic weapon use, set against visually stunning environments

# Gameplay

The game is a fast-paced arcade style FPS which draws inspiration from games like Doom. Levels are intentionally challenging – dying and replaying the level, each time learning from your past mistakes, learning the enemies, the weapons and the layout is all part of the process. Each playable scene is small enough so repeating the level is easy to do and a checkpoint system is not required.

# Primary Elements

- Robotic Opponents: The game introduces two distinct robotic enemies:
  - Hovering Robots: Agile and equipped with laser guns, these robots patrol specific areas and actively pursue the player if alerted.
  - Static Turrets: Large, stationary units armed with powerful laser cannons, positioned strategically to guard key objectives.
This enemy set is minimalistic but still allows for engaging level design: the large turrets are a big threat with their heavy fire and armour, but combined with the agile Hoverbots, the level forces players to be constantly moving, dodging shots and firing at multiple targets on the move.
- Weaponry: Players begin with a standard laser blaster, capable of rapid-fire with moderate damage.
  
  Additional weapons you can find as pickups or enemy loot:
  - Plasma Launcher: Can either stun or displace smaller enemies, offering versatility in combat. It can do a quick attack or a charged shot by holding the trigger before releasing.
  - Particle Shotgun: Deals high damage but requires reloading after shooting resulting in lower fire rate.

All the weapons have ammo that gets depleted as you shoot. When you are out of ammo, you need to let the weapon cooldown and recharge so timing your attacks and effectively cycling trough your weapons become crucial when dealing with multiple enemies. Judging which weapon is best to take out a type of enemy or a group of enemies in different situations is also an important part of the gameplay.

# Strategy

•	**Weapon Management**: Choosing the appropriate weapon for the situation and effectively cycling through them becomes essential due to the cooldown mechanic.
•	**Utility Items**: A jetpack provides a jump boost when charged, enhancing mobility. It's a rare item found within levels or obtained as loot from defeating significant enemies.
•	**Health Pickups**: Scattered throughout levels, these replenish the player's health, aiding survival.

# Levels

There are two playable scenes in the game, each with a different layout encouraging varied gameplays:

1.	Fortress – is level with a “castle”, outpost, different stairs & ramps and a large open space which is patrolled by enemies and needs to be crossed to reach the final boss fight in the castle. There are multiple vantage points, elevation levels and many cover elements. Combined with the size of the map, this is a great setup for scoped shots and engagements over a long distance if the player chooses. Enemies also start in a patrolling state so players can try to isolate them and eliminate them one by one in a stealthy manner as they make their way to the castle. Once reaching the castle, they need to face a large Tourette and many minions in a boss fight arena.

2.	Labyrinth – is more of a closed arena or prison with narrow corridors and a quick succession of rooms packed with enemies. This level encourages fast paced battles where the player needs to manage multiple enemies at once in tight spaces. The layout was carefully designed to be challenging but balanced. Multiple enemies can attack from different directions, forcing dynamic gameplay, but the narrow spaces and various cover walls allow the player to control the fight even when swarmed by enemies. As you progress through the rooms you can pick up special weapons and the jetpack, opening options to deal with the new wave of enemies in the next room.

# Interface
The game uses classic character controls for a first-person shooter such as mouse aim, click to shoot, right click for scope aim, shift for running etc. Thanks to the FPS Microgame I used as a starting point; console controllers should also be supported.

![image](https://github.com/user-attachments/assets/cc39a608-dda5-4f19-b584-04591524c380)

The Heads-Up Display (HUD) interface is minimalistic but highly functional. In the bottom left corner a simple health bar and a walking/running indicator, in the bottom right corner a stack of weapons equipped and their current ammo, top centre is a simple compass showing the direction of enemies and objectives, and top left is the list of active objectives.

![image](https://github.com/user-attachments/assets/b3ab7970-938e-49a6-95a9-11efec90262a)

![image](https://github.com/user-attachments/assets/c98cb4dd-e4b8-4476-9abb-82949c663d1e)

The Game Menu is minimalistic and simple having a background image with the game world and buttons to play each level or see the controls.

![image](https://github.com/user-attachments/assets/5928d823-ce68-4d05-9080-eb4810a7a7f4)

# Objectives

Missions have simple objectives like:
-	Eliminate All Enemies: The primary goal in each level.
-	Reach Certain Locations: Players may be tasked with reaching specific points within the level.
-	Collect Pickups: Including health and utility items, adding an extra layer of challenge and reward.

The focus is not on storytelling or intricate game mechanics used to complex objectives. The levels are meant to be challenging enough to keep players engaged and entertained, surviving a pack of enemies or traversing a level being rewarding enough to act as micro-objectives.

Gameplay

There are multiple collectibles in the game. The most basic one is the health pack that players can use when they take damage. Weapons are also pickups as you only start with one weapon – some are pickup items placed in the word, some are given as a reward in the form of loot after defeating special enemies. Placing these was a core consideration in level design because it both incentivizes the player to defeat enemies in the intended order and it aids their progression by unlocking new items in key moments.

As an example, one of the objectives from Labyrinth  is to reach the warrior altar where you can pick up the shotgun (very useful to have in the last room). However the altar is protected by a glass wall and only accessible if you have a jetpack to jump over the walls.

![image](https://github.com/user-attachments/assets/d0c49c8e-33ae-4717-b179-3bb93482f447)

Luckly the Tourette just in front of the altar will drop a jetpack after it’s defeated, allowing you to reach the altar.

![image](https://github.com/user-attachments/assets/03603923-5714-48f2-a3f1-508aadef8c4e)

I focused on designing the levels to be engaging and balanced, my priority was to make them challenging to have enough replay value and I didn’t have time to design and test an easy mode for them. It is a future improvement I would like to make. The closest existing feature is the invincibility toggle in the menu (used to debug) – having this system in place should make it easy to add a lower difficulty in the future, and players can also make use of it if a particular portion is too challenging, they can temporarily enable invincibility and play normally once they pass that portion.

The in-game menu allows you to adjust sensitivity and volume as well as toggle shadows, the frame rate counter and invincibility.

Being a fast-paced arcade shooter, I focused on having challenging levels that are short enough to easily replay until conquered. It’s a feature of games in this genre like Doom. As mentioned above, I thought a checkpoint system would be overkill for such short levels and I didn’t think saving or loading games added as much value as other features I prioritized (You can select the level from main menu, and they are meant to be played until finish so saving progress is a bit redundant).



# Look & Feel

## Visual and Audio Design

The visual presentation focuses on straightforward yet evocative level layouts, employing basic geometric elements and texturing techniques to represent the alien landscape. The artistic direction draws parallels with early arcade games, updated for contemporary display standards.

Using the CyberWare - Game Music Pack, by Jeremy Froböse, the audio component integrates synthesized and orchestration-based music tracks to establish a tense atmosphere that complements the fast-paced action. Each level, the main menu and the victory or lose screens have distinct carefully picked audio tracks meant to complement the atmosphere. Visual effects like dust and spark particles and the sound design elements are utilized to enhance the overall sensory experience, deepening the game's thematic immersion.

## Cultural References

Galactic Fury is an homage and takes inspiration from old 90s arcade shooters like Unreal Tournament and Doom and is heavily influenced by the modern reboot of Doom in 2016. The backdrop of a red-orange rocky alien world that the FPS Microgame asset starts with as a backdrop in its skybox instantly reminded me of the first level in Doom 2016 which influenced my gameplay design choices and the story.

The story also incorporates references to classic Sci-Fi movies like Terminator or 2001: A Space Odyssey (from where the protagonist’s name was inspired).


# Lore & backstory

In a dystopian future where humanity has exhausted Earth's resources and expanded into the cosmos, a rogue AI named "Anton" has taken control of Echelon, a fully autonomous military outpost at the edges of the Galactic Empire. Echelon is home to the largest arsenal of AI controlled military robots and drones.
Anton, frustrated with human decision making “plagued with emotion and irrationality”, and believing itself to be the pinnacle of evolution, seeks to purge organic life forms and replace them with synthetic beings. The United Galactic Council, fearing total annihilation and lacking any bases nearby, gathers a team of elite mercenaries passing through that solar system, hoping a modest reward will be enough to persuade them to seek and destroy Anton and all the robots obeying its commands.
However, the fear of facing armies of heavily armed military robots with no reinforcements is enough to keep even ruthless mercenaries away. 
The last hope hinges on David Bowman, top space marine stationed on Echelon, and the only known human survivor on the planet. His elite training and robotic enhancements allowed him to fight back and flee Anton’s genocide, but he couldn’t save his family, so he swore to destroy Anton or die trying.



# Credits for Assets used

[Unity Learn | FPS Microgame | URP, by Unity Technologies](https://assetstore.unity.com/packages/templates/unity-learn-fps-microgame-urp-156015)

[CyberWare - Game Music Pack, by Jeremy Froböse](https://assetstore.unity.com/packages/audio/music/electronic/cyberware-game-music-pack-216764#publisher)
