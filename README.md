# ONI-Modloader
A simple mod loader for **Oxygen Not Included** based in Harmony

[**Forums in Klei**](https://forums.kleientertainment.com/topic/88186-mod01-oni-modloader/)


Disclaimers
-----------
* Please DON'T REPORT BUGS you encounter to Klei while mods are active.
* BE AWARE that many of the mods are still a WIP and may fail. If you are having problems use a clean ONI installation and try to test the mods one by one to narrow the error. Then post a issue in github.
* We do not take any responsibility for broken saves or any other damage. Use this software at your own risk.
* If you load a savegame, it requires that you have exactly the same mods when you saved it.

This project uses source code of and is based on: [Harmony](https://github.com/pardeike/Harmony), [ModLoader Installer](https://github.com/zeobviouslyfakeacc/ModLoaderInstaller), [Besiege Modloader](https://github.com/spaar/besiege-modloader), [OnionPatcher](https://forums.kleientertainment.com/topic/81296-mod159-materialcolor-onionpatcher/)


**NOTE**: Compiled for **Q2-311032**

**Report Bugs** for ONI-Modloader here: https://github.com/javisar/ONI-Modloader/issues


Mods based in Harmony
---------------------
* [**Javisar's Mods**](https://github.com/javisar/ONI-Modloader-Mods) [Forum](https://forums.kleientertainment.com/forums/topic/97444-mods-trevices-mods-lair/)
* [**Cairath's Mods**](https://github.com/Cairath/ONI-Mods) [Forum](https://forums.kleientertainment.com/forums/topic/94120-mods-cairaths-mod-corner/)
* [**Rainbow's Designs Mods**](https://github.com/rainbowdesign/OxygenNotIncluded-Mods) [Forum](https://forums.kleientertainment.com/forums/topic/95313-rainbowdesigns-mods/)
* [**MidnightSteam's Mods**](https://github.com/Midnight-Steam/ONI-Modloader)
* [**MooreDavid's Mods**](https://github.com/MooreDavid/ONI-MOD-) [Forum](https://forums.kleientertainment.com/forums/topic/96381-seekers-modding-bucket/)
* [**Sijko's Mods**](https://github.com/Sijko/ONI-Mods/) [Forum](https://forums.kleientertainment.com/forums/topic/95988-mods-small-mods/)
* [**Blindfold's Mods**](https://github.com/Blindfold-Games/ONI-Blind-MODS)
* [**EtiamNullam's Mods**](https://github.com/EtiamNullam/Etiam-ONI-Modpack) [Forum](https://forums.kleientertainment.com/forums/topic/101902-mods-etiams-modpack/)
* [**AntiBlueQuirk's Mods**](https://github.com/AntiBlueQuirk/ONI-MaterialProbeMod) [Forum](https://forums.kleientertainment.com/forums/topic/103110-mods-material-probe/)
* [**lfricken's Mods**](https://github.com/lfricken/oni-mods) [Forum](https://forums.kleientertainment.com/forums/topic/103271-lfricken-mods/)

For **Mod Request to the Community** post them in [Klei Forums](https://forums.kleientertainment.com/forums/topic/88186-mod05-oni-modloader/) or in [ModLoader GitHub](https://github.com/javisar/ONI-Modloader/issues/new?template=feature_request.md).


Quick Start
-----------
1. Download the [**Latest Version**](https://github.com/javisar/ONI-Modloader/blob/master/Managed/ModLoader.dll)
2. Copy ModLoader.dll to ONI Managed folder:
   * Windows: \OxygenNotIncluded\OxygenNotIncluded_Data\Managed\
   * Mac: /OxygenNotIncluded/OxygenNotIncluded.app/Contents/Resources/Data/Managed/
3. Move your mods to the Mods folder:
   * Windows: \OxygenNotIncluded\Mods\
   * Mac: /OxygenNotIncluded/OxygenNotIncluded.app/Contents/Resources/Mods/
4. Start your game and check for [logs](http://support.kleientertainment.com/customer/portal/articles/2744766-logs-and-useful-information-for-bug-reports) in output_log.txt or Player.log.


How it works
------------
* The MODLOADER loads C# Harmony Patcher and also all Harmony Based mods in /Mods/ path.


Installation
------------
0. Prerequisites:
   * Make SURE you're using the latest version from Github main branch.
   * Make SURE you're using a fresh install of ONI. Check [Verify Integrity Files](https://inxile.zendesk.com/hc/en-us/articles/115004662908-Verify-game-cache-files-Steam-) function in Steam in the ONI game Properties>LocalFiles tab.
   * Make sure you deleted all previous modloader file in:
     * Windows: \OxygenNotIncluded\OxygenNotIncluded_Data\Managed\
	 * Mac: /OxygenNotIncluded/OxygenNotIncluded.app/Contents/Resources/Data/Managed/
1. Click "Clone or Download" and "Download ZIP" for the current version as the releases may not be up to date.
2. Copy the contents of the "Managed" folder to the folder:
   * Windows: \OxygenNotIncluded\OxygenNotIncluded_Data\Managed\
   * Mac: /OxygenNotIncluded/OxygenNotIncluded.app/Contents/Resources/Data/Managed/
3. Create "Mods" folder in the ONI main directory.
   * Windows: \OxygenNotIncluded\Mods\
   * Mac: /OxygenNotIncluded/OxygenNotIncluded.app/Contents/Resources/Mods/
4. Check for error logs in:
   * \OxygenNotIncluded\OxygenNotIncluded_Data\Managed\Mod_Log.txt   


Uninstallation
--------------
Remove ModLoader.dll from \OxygenNotIncluded\OxygenNotIncluded_Data\Managed\ folder.


[Mods Installation](https://github.com/javisar/ONI-Modloader-Mods/blob/master/README.md#mods-installation)
-----------------


Requirements
------------
* .NET Framework v3.5
* Harmony Patcher v1.2.0.1
* Visual Studio 2015


Creating a Mod
--------------
0. Feel free to mess with any of the mods from https://github.com/javisar/ONI-Modloader-Mods
1. 'Clone or download' the project from the mod repo.
2. Copy the following files from ONI Managed folder '\OxygenNotIncluded\OxygenNotIncluded_Data\Managed' to the mod solution folder '\Source\lib\'
   * UnityEngine.dll
   * UnityEngine.CoreModule.dll
   * Any needed unity UnityEngine.*.dll   
   * Any needed ONI Assembly-CSharp-*.dll
3. Open the solution with Visual Studio.
4. Create a new class project. 
   * To create a Project from scratch the right one is: Visual C#-Class Library (.NET Framework). 
   * If you don't find it like when you have installed Visual Studio with Unity you need to tools-add tools or features and install: .NET Desktop Development.
   * It's available a **[Visual Studio Project Template](https://github.com/javisar/ONI-Modloader-Mods/blob/master/Source/TemplateMod.zip)**
     * Copy the .zip file to ~\Documents\Visual Studio 2019\Templates\ProjectTemplates\Visual C# to access the template in VS
5. Add the previous libs as references of the project.
6. Compile it to generate the mod dll file.
7. Check the tutorials at the end of the page.
   * Harmony is a code injector which will help you to inject your .dll with the help of the modloader.
8. If you want to go into the ONI code you need to peek with a decompiler like JetBrains dotPeek or ILSpy.
9. If you need more help please ask at [The Discord Server in the Modding Channel](https://discord.gg/EBncbX2)

**Note**: Dlls will be recognized by the mod loader if they reside in the main mod directory and subfolders.


How to debug mods
-----------------
**SIMPLE (recommended)**
The easier way to debug a mod is to use the Unity debug logs:
* Include in your VS project references the library from ONI managed folder: UnityEngine.CoreModule
* Insert in your code log dump lines like:
   Debug.Log("...");
* Check for the [logs](http://support.kleientertainment.com/customer/portal/articles/2744766-logs-and-useful-information-for-bug-reports) in output_log.txt or Player.log

**ADVANCED**
* Check in output_log.txt the Unity version used by ONI. Look for it in the first lines: Example: Initialize engine version: 2018.2.7f1
* Download from [here](https://github.com/0xd4d/dnSpy/releases) the corresponding "mono.dll" file. This is mono modified to enable debugging.
* Replace mono.dll in ONI folder: \OxygenNotIncluded\Mono\EmbedRuntime\
* Visual Studio
   1. Install Unity for Visual Studio
   2. Configure your VS project to output Debugging Info. You must generate .pdb file with complete info.
   3. Compile your project
   4. Execute "lib\pdb2mdb.exe name.dll". This will generate in the same folder a .mdb file. "pdb2mdb.exe" for VS can be found [here](https://gist.github.com/jbevain/ba23149da8369e4a966f)
   5. Exe, pdb and mdb files must be in Mods ONI folder.
      * If you use the **[Project Template](https://github.com/javisar/ONI-Modloader-Mods/blob/master/Source/TemplateMod.zip)**, steps 4 and 5 will execute as a script automatically after the mod is rebuilt
   6. Run Oxygen Not Included.
   7. In VS, select option "Attach to Unity Debugger" and enter the IP: 127.0.0.1:55555
   8. Now your VS must be connected to the Game and stop in your breakpoints.
* dnSpy
   1. Follow this [guide](https://github.com/0xd4d/dnSpy/wiki/Debugging-Unity-Games)


Tutorials
-----------------
* https://github.com/pardeike/Harmony/wiki/
* https://github.com/roxxploxx/RimWorldModGuide/wiki/SHORTTUTORIAL:-Harmony
* https://github.com/UnlimitedHugs/RimworldHugsLib/wiki/Introduction-to-Patching
* https://github.com/UnlimitedHugs/RimworldHugsLib/wiki/Detouring
* https://oxygennotincluded.gamepedia.com/Guide/Working_with_the_Game_Files
* https://github.com/Mpstark/ModTek/wiki/Writing-ModTek-DLL-mods
* [Transpiler Tutorial](https://gist.github.com/pardeike/c02e29f9e030e6a016422ca8a89eefc9)
* https://github.com/blushiemagic/tModLoader/wiki/Another-Simple-Harmony-Transpiler-Tutorial
* [Harmony Transpiler Help](https://ludeon.com/forums/index.php?topic=36406.0)
* https://rimworldwiki.com/wiki/Modding_Tutorials/Decompiling_source_code


Downloads
---------
Choose 'Clone or Download'.



