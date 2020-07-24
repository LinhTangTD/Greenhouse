# Greenhouse

Greenhouse is an educational game that aims to teach player how to make decision using data. The game allow players to grow and sell various crops, while also determining the proper amount of water, fertilizer and pesticides that should be used for each crop in each season. Players can choose any options they like, but they increase their chances of making profit if they thoroughly understand the data and techniques for analyzing it.

The game growth models for Iowa farmland. Each plot represent approxiamately one tenth and acre and the yields for each crop are measured in bushels.

Greenhouse is developed in Unity and C# by [Linh Tang](https://linhtang.me/), [Yolanda Jiang](https://github.com/yolandajhzm) and Zhaoqing Wu under the mentorship from professor Shonda Kuiper. 

  ➤ [Play Game](https://www.stat2games.sites.grinnell.edu/games/greenhouse.html)
  
  ➤ [Instructor Notes](https://stat2labs.sites.grinnell.edu/farmer.html)

  ➤ [Greenhouse Tutorial](https://youtu.be/uIc2_2b4lAE)
  
  ➤ [Data Visualization App](http://shiny.grinnell.edu/Greenhouse_Visualizations/)

  ➤ [Game Data Request](https://stat2games.sites.grinnell.edu/data/greenhouse/greenhouse.php)

  ➤ [See All Similar Games](https://stat2games.sites.grinnell.edu/)


## How to play?

There are 5 different levels in the game, each level is built upon different settings to the farm. The goal is to test various combinations of water, crop, fertilizer, etc. whether they are profitable. Throughout the game, multiple data visualizations can be used to understand the optimum amount of water and fertilizer needed for each crop. In addition, sunlight, pest infestations, and changing market prices can make it even more difficult to earn profit. 

The game can be played in any web browser that supports HTML5. Users also need mouse and keyboard to play this game.

## For developers

  ➤ Source code and resources is posted at the `KuiperResearch\Posted Games` folder within Grinnell College storage network. For more information about the copyright and access, please contact professor Shonda Kuiper.
  
We use [Visual Studio](https://visualstudio.microsoft.com/) to code and edit `C#` scripts and [Unity](https://unity.com/) version `2019.3.14f1` to build the UI of the game.

We also use [SourceGear DiffMerge](https://sourcegear.com/diffmerge/) as the revision control tool to support difference comparison between different version in `UnityCollab`.

### Getting Started
Install Unity and Visual Studio for developing environment. Open the project with Unity Editor. You can see all objects of the current scenes in `Hierarchy` tab on the left. The `Inspector` tab on the right is where all the property of the objects can be edited. Under the `Project` tab is all the files in your project folder. The middle panel includes 3 tabs, `Scene` and `Game` which let you view the game in editor and player mode, and `Console` lists out errors, warnings when running the game.

Check your settings to make sure that your current platform is WebGL before building. (From the menu: `File` -> `Build Settings...`)

### Project Hierarchy
Neccesary files for development can be found under the `Assets` folder with name-self-explanatory subfolders: `_Prefabs`, `_Scenes`, `_Scripts`, and `Contents` where most of the sprites and materials (images, sounds, video, etc) are stored.

### Game Structure
There are 7 scenes in this game:
 
  ➤ `Main Menu` is the starting scene of the game where players enter their playerID, groupID and choose the level that they want to play. This scene is linked to and from `Instructions`, `Credit` or `LevelComplete`.

  ➤ `Instructions` provides users with the settings specific with the level they choose. After the players enter their PlayerID, GroupID and choose the level in `Main Menu`, this scene will show up with corresponding settings. This scene can be entered from `Farm` or `Main Menu` and can lead to `Farm` or `Scatterplot`.

  ➤ `Farm` is the main scene with most complex functions and models. This is where all the farming activities take place. This scene is linked to and from from `Instructions` or `LevelComplete`.

  ➤ `LevelComplete` shows up at the ends of each season after players finish growing, harvesting and selling all their crops. This notifies players of their performance in the latest season. This scene can be entered from `Farm` and can lead to `Main Menu`, `Instructions`, or `Scatterplot`

  ➤ `Scatterplot` contains the graph visualizing player's data when playing the game. This scence can be entered from `LevelComplete` or `Farm` and can lead to `LevelComplete` or`Farm`.

  ➤ `Selection` is used for Level 4 where users. This scene is only accessed when players choose Level 4 from `Main Menu` and can lead to `Farm`.

  ➤ `Credits` is linked to and from `Main Menu`, providing information about creators, contributiors, assets used and resources link.

## Contacts
[Linh Tang](mailto:tanglinh@grinnell.edu) | [Yolanda Jiang](mailto:jianghui@grinnell.edu)