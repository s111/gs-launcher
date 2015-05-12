# Launcher
The launcher is the part of the system where you choose which game you want to play.
It is designed exactly like a game, and is handled as such by the back end.
This means that the launcher application is actually a game that displays a list of the available games, and provides an interface for the players to start a game.
Using the controller on their smartphone a player can browse through the games, and eventually select one of them to play.

## Table of Contents

- [Precompiled](#precompiled)
- [Develop](#develop)
- [Compile and package](#compile-and-package)
- [Screenshots](#screenshots)
	- [Launcher](#launcher)
	- [Controller](#controller)

## Precompiled
The game packaged together with the controller.  
[Linux](https://github.com/s111/gs-launcher/releases/download/v1.0/launcher_linux.zip)  
[Windows](https://github.com/s111/gs-launcher/releases/download/v1.0/launcher_windows.zip)  
[All Releases](https://github.com/s111/gs-launcher/releases)

Unzip and the ```launcher``` folder can now be added to the game systems ```games``` directory.

## Develop
Download the repository:
```sh
git clone github.com/s111/gs-launcher
```

Download [NW.js](http://nwjs.io/)

Run the launcher:
```sh
cd gs-launcher/game
nw .
```
Remember that you need the game system running in the background for it to work.

## Compile and package
Download [NW.js](http://nwjs.io/)  
Refere to https://github.com/nwjs/nw.js/wiki/How-to-package-and-distribute-your-apps for how to make an executable launcher.exe from the files in ```gs-launcher/game```.

Copy ```game.json```, ```screenshot.png``` and the ```controller``` folder into the ```launcher``` folder. Now copy the launcher executable (```launcher``` on linux and ```launcher.exe``` on windows) and the files required by NW.js into the  ```launcher/bin``` folder.

You should now have a folder named ```launcher``` which looks something like this:
```
launcher/game.json
launcher/controller/index.html
launcher/controller/controller.js
launcher/bin/launcher.exe
launcher/bin/nw.pak
launcher/bin/...
```
This folder can now be added to the game systems ```games``` directory.

## Screenshots

### Launcher
<img src="https://github.com/s111/gamesystem/blob/master/screenshots/launcher.png" width="640">

### Controller
<img src="https://github.com/s111/gamesystem/blob/master/screenshots/launcher_controller.png" width="320">
