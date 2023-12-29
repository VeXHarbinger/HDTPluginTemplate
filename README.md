# Preface

## Purpose

This project should help jump start your development of your own plug-in for the [Hearthstone Deck Tracker](https://github.com/HearthSim/Hearthstone-Deck-Tracker)
![Display Example](https://raw.githubusercontent.com/VeXHarbinger/HDTPluginTemplate/master/images/PluginDisplay.png)


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

## Debugging

if $(ConfigurationName) == Debug (
  copy "$(TargetDir)$(ProjectName).*" "\HearthstoneDeckTracker\Plugins" /y
)

## Publishing
What to remember to do when publishing
* Remember to set your VS Build to release
* Open your bin\release folder, 
 * Right Click on ONLY your plugin.dll and select compress to zip
 * If there are additional .dll files in this folder, make sure all of the project references have the local copy setting, set to False
 * .dlls from NuGet Packages will be in here, just ignore them.  

# Links

## Documentation
* [Creating a Plug-in](https://github.com/HearthSim/Hearthstone-Deck-Tracker/wiki/Creating-Plugins)

* [ThemeManager](https://github.com/ControlzEx/ControlzEx/blob/develop/Wiki/ThemeManager.md)



[![GitHub Latest](https://img.shields.io/github/release/VeXHarbinger/HDTPluginTemplate.svg)](https://github.com/VeXHarbinger/HDTPluginTemplate/releases/latest)
[![Github All Downloads](https://img.shields.io/github/downloads/VeXHarbinger/HDTPluginTemplate/total.svg)](https://github.com/VeXHarbinger/HDTPluginTemplate/releases)