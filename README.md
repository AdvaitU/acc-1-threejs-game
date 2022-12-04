# acc-1-threejs-game
Video game prototype created as the final project for Advanced Creative Coding-1 at CCI.

Find a video demonstration here: 
Link to GitHub Repo: https://github.com/AdvaitU/acc-1-threejs-game
Link to MIMIC Project Build: https://mimicproject.com/code/0d7dc9c2-37dc-d5db-5d56-1e19e1c50f24

PROJECT INTRODUCTION
For a while now, I've been toying with the idea of creating a first person detective game. , one that allows a player free reign but almost no information when dropping them into a world frozen in time. The player can then move around the world as they see it, discovering the stories waiting to be told through a series of object-specific clues. These clues include newspaper articles, excerpts from books, screenshots from Youtube, copies of travel tickets and governmental permits, text chains between the people in this world, scientific papers, etc. These clues can be obtained in any order by travelling to any object in the scene and reading things that pop up. The game works by crafting a story but only telling it thropugh disorganised snippets gathered in random orders and watching the player piece it together one by one. Ideally, an endpoint of solving the mystery would exist but doesn't in this prototype due to constraints in time and technical ability. But only upwards from here :D

ABOUT THIS PROTOTYPE
The prototype (POC) is built in threejs and uses inbuilt threejs geometries to build out a number of objects such as planets, satellites, spaceships, shields, bullets, etc. Although limited currently, I see a final version that I can afford more time to having a vastly more intricately crafted scene. The current programme is habited by 5-6 spaceships of two different kinds, rockets, planets, and satellites along with a unique 'hero' ship, bullet and shield animations and a randomly generated array of celestial bodies floating around in space. The player can use standard orbital controls to navigate the scene. When the player is within a 50x50x50 cuboidal distance from an object, the object pops up a sprite created in Adobe Illustrator that acts as the aformentioned 'clue'. The webpage also plays a sound unique to the object in addition to the deep space background track.

ABOUT MY PROCESS - EXPERIMENTATION
The entire project hinged on creating a system that coulkd detect collisions between the camera (player) and the object in the scene. Thanks to a few tutorials on YouTUbe and the documentation at threejs.org, I was able to build a system of Bounding Boxes around all objects as well as a large bounding box that wraps around the camera in the scene. When the camera bounding box intersects another object's bounding box, a sprite is inserted into the scene using the box3.intersects(box3) method conditional. While it is certainly not the most elegant system, I'm proud of having created it 3 weeks into first hearing the world threejs :). Apart from the collision detection system, I explored threejs documentation to did a series of other experiements that add to the scene. Some of my favourites that I found the most fun to do are:

1. Bump Maps! - Who knew putting a black and white seemingly random looking JPEG in my programme could help create such intricate surfaces! (Most programmers I assume, 
                but I didn't hehehe)
2. Sprites! - Creating PNGs with transparent backgrounds that I can then place in the scene in such a way that they always face the camera was perfect for the 'pop-ups 
              I was visualising!
3. Cloning and Grouping Objects: Cloning, Grouping and using the .setFromObject method were a game-changer once I discovered them! They helped organise a process that, 
                                 at first, seemed long and daunting.
4. Fog Exp 2 - At first, once I'd created the world with a Skybox like in the homeworks, it seemed rather unrealistic. Discovering the Fog object really helped light 
               the world the way I imagined it.
5. Random Generation of Celestial Bodies - After the main objects went into the scene, I wanted to create 'dust' that sat around the scene and gave it a sense of 
                                          motion. I wrote s tiny function to create randomness using the Math.random method for the purpose and it definitely paid off.
6. Parent-Child - Helped with creating the motion in satellites and the Celestial bodies very efficient.
7. Extrude Geometry - When inbuilt geometry wasn't enough and I was refraining from creating and importing models from CAD so as to explore threejs as much as I could, 
                      drawing shapes and extruding them helped create the vision I had for the Control Rooms in the scene.
8. Audio Loader - Helped wrap the scene up and really create the environment I was looking to invoke.




