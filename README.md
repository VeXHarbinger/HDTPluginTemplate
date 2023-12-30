# Preface

## Purpose

This project should help jump start your development of your own plug-in for the [Hearthstone Deck Tracker](https://github.com/HearthSim/Hearthstone-Deck-Tracker)  

![Example Plug-In Display](https://github.com/VeXHarbinger/HDTPluginTemplate/blob/master/Images/PluginDisplay.png)


## Helpful Plug-Ins

 * [MarkdownEditor2](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.MarkdownEditor2), which will also help you can read this easier in the IDE.  
 * [XAMLStyler](https://marketplace.visualstudio.com/items?itemName=TeamXavalon.XAMLStyler)  
 * [OpenInExplorer](https://marketplace.visualstudio.com/items?itemName=Charles-Ant.OpenInExplorer2022)  


#  Development

## Configuration

* Get Latest versions of HDT and HearthDb
  * Copy them to the lib folder
  * Verify the project reference versions
* Set Plug-in Assembly Version
* Press Ctrl+w,t to see the ToDo list.  Make sure to delete any example functionality you don't want to keep 

![Versions](https://github.com/VeXHarbinger/HDTPluginTemplate/blob/master/Images/LibVersioning.jpg)


### Create a Build Event

  You can create a build event in the project's properties to publish your plug-in .dll into your HDT plug-in folder.  
  This way you can just do a debug build and then fire up your HDT to test it out.  
  **Remember**, you have to restart HDT after you build a new .dll to clean out the old version from the session memory.  

`if $(ConfigurationName) == Debug (  
   copy "$(TargetDir)$(ProjectName).*" "\HearthstoneDeckTracker\Plug-ins" /y  
)`

### Debugging 

You can attach your VS debugger to a running HDT session by pressing  Ctrl+Alt+P, then select HearthstoneDeckTracker from the list of running processes.  
You can press Shift-Alt-P to reattach to the process after the first debugging session to skip the selection window.  

![Attach To Process](https://github.com/VeXHarbinger/HDTPluginTemplate/blob/master/Images/attachToProcess.jpg)  

**Remember** to click the Show Threads in Source (or ensure it's enabled) once the debugger starts  

![Show Threads In Source](https://github.com/VeXHarbinger/HDTPluginTemplate/blob/master/Images/ShowThreadsInSource.png)  



## Publishing

What to remember to do when publishing  
* **Remember** to set your VS Build to release  
* Open your bin\release folder,  
 * Right Click on ONLY your plugin.dll and select compress to zip  
 * If there are additional .dll files in this folder, make sure all of the project references have the local copy setting, set to False  
 * .dlls from NuGet Packages will be in here, just ignore them.  

# Links

## Documentation

* [Creating a Plug-in](https://github.com/HearthSim/Hearthstone-Deck-Tracker/wiki/Creating-Plugins)  
* [ThemeManager](https://github.com/ControlzEx/ControlzEx/blob/develop/Wiki/ThemeManager.md)  


## Acknowledgments

Wanted to say thanks for the great work they did to pave the way for me.  

# Stats

[![GitHub Latest](https://img.shields.io/github/release/VeXHarbinger/HDTPluginTemplate.svg)](https://github.com/VeXHarbinger/HDTPluginTemplate/releases/latest)
[![Github All Downloads](https://img.shields.io/github/downloads/VeXHarbinger/HDTPluginTemplate/total.svg)](https://github.com/VeXHarbinger/HDTPluginTemplate/releases)