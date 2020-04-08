# Jamie's Mod for HLVR
This is the start of my attempt to recreate at least one map of [Jamie's Mod](https://www.moddb.com/mods/jamies-mod) in HLVR.
You can see a gameplay clip from one stage of development [here](https://www.youtube.com/watch?v=JMqgsJd87hE).

## What is this?
This is a sourcemod for the [hlnonvr](https://github.com/Jan4V/hlnonvr) mod for HLVR by Jan4V. You can still run it in vr mode using the parameter ``-vr`` (provided using batch files in releases). So far some custom things that have been made in-engine include:
* A (mostly) ported Half-Life: Source map
* Custom models (Jamie's Barney model for example)
* Custom textures (Jamie/HL1 textures)
* Custom sounds (Custom soundscript to include Jamie/HL1 sounds)
* Custom "NPCs" (prop_dynamics that can be damaged and moved based on the custom models' animations)

## How do I install this?
You must install [hlnonvr](https://github.com/Jan4V/hlnonvr) first (there should be a tutorial on the GitHub page). Afterwards, just take a release and drag the files into the ``Half-Life Alyx`` directory. You should not need to replace any files to get it to work due to the nature of sourcemods. Once that's done, just launch ``launch-jmod.bat`` or ``launch-jmod-vr.bat`` to start the game.

## How do I start development?
I suggest using the [unofficial SDK](https://github.com/gvarados1/Half-Life-Alyx-SDK) by gvarados1 if you'd like to start development. You need to install [hlnonvr](https://github.com/Jan4V/hlnonvr) in the SDK and launch the SDK with the parameter ``-game jmod``.

You'll also need to recompile /pack/ into a [VPK file](https://developer.valvesoftware.com/wiki/VPK), I suggest using vpk.exe from Source SDK Base 2013 as I've had the most luck with it. Once it's a VPK file, move and rename it to ``/game/jmod/jamie.vpk`` for it to be recognized. This VPK file is to replace HLVR/Core content with custom content as stated in the gameinfo.gi file. Be aware that the gameinfo will differ between release (jmod_dist) and development (jmod) as content is loaded differently between the SDK and HLVR, take a look at a release gameinfo.gi file for more information.

## Current goals:
* Add scientists
* Add doors and moving parts
* More interactable things (so far I made two HL1 books physics objects)

## Future goals:
* Replace Alyx/Russell speech
* Replace Alyx's hand models
* Replace weapon models
* Replace stock HLVR sfx
