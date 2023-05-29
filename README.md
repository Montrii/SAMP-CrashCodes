# SAMP-CrashCodes

Contains a list of error codes when having SAMP Crash.

Error: 0x004A8E3E

Problem: Removing an item from a list. The "backtrace" at the end of the crash log can help to understand the type of the list. If it has "0x005A328B" just below it, it's related to procobj.dat mods.
Solution: Possibly procobj.dat limit, or some other bug caused by procobj.dat mods. There are indications that it is procobj.dat file merge bug in modloader as well.

Error: 0x00801C3B

Problem: List allocation. It can be caused by many different reasons, "backtrace" might help something.
Solution: It was already caused by the collision model of an airplane, changing the collider (or the vehicle model itself) solved it.

Error: 0x004C53D4

Problem: Getting a part/dummy from a vehicle. Probably related to tuning parts?
Solution: Identify if it is a problem with some car mod or script, if there is 0x00469FF7 in the backtrace it is some CLEO mod and SCRLog can help.

Error: 0x0156173D

Problem: Limit of ColModels (collision models inside vehicle .col or .dff files).
Solution: Increase the limit by installing Open Limit Adjuster or configuring the fastman92 limit adjuster.

Error: 0x004C705A

Problem: Related to building the collision model of a person's body (usually used when there is a shot and you need to determine if it hit a person's limb).
Solution: Identify and remove, contact the author etc of some skin mod, there may be something wrong in the .dff of the model.

Error: 0x004AA393

Problem: Related to stop playing a special effect (such as smoke, fire, explosion, etc).
Solution: Identify which mod, if it's an effects mod, the backtrace at the end of the log can help if it's an asi mod, scrlog can help if it's a CLEO mod etc.

Error: 0x01564BC8

Problem: Limit of pickups or some mod tried to work with a pickup that doesn't exist or invalid value.
Solution: Identify which mod, SCRLog can help you, remove it and contact the author, or increase the limit if necessary.

Error: 0x005C09F6

Problem: Some misconfigured effect mod (couldn't read the PRIM section). .fxp or .fxs files.
Solution: Identify which mod, which effect, try to fix it, contact the author, etc.

Error: 0x00537F0D

Problem: Unable to load a model's bounding box from a .col file.
Solution: Identify which .col file, from some mod, is causing this, it's probably badly edited, poorly created, etc.

Error: 0x006D3B64

Problem: Some CLEO mod hitching a vehicle/trailer that no longer exists.
Solution: SCRLog can help identify, probably.

Error: 0x009654DA

Problem: Something related to pedgrp, when trying to load some new ped model for gangs.
Solution: Something about pedgrp limit and gang models? Any invalid models?

Error: 0x00B4C2DD

Problem: Something related to the built-in special effects in .dff files (2dfx).
Solution: Some badly edited, poorly made .dff, or is probably related to 2dfx limits, something about that.

Error: 0x004C4C7E

Problem: Error reading a map model that has some special effect built into the .dff.
Solution: Probably one of these .dff files has a problem, badly made, badly edited, etc.

Error: 0x00409436

Problem: The in-game camera no longer exists and thus caused a problem when trying to load new models to the map.

Error: 0x0040B659

Problem: When trying to start loading a new vehicle model, the person.
Solution: Any bad cargrp or pedgrp configuration? Some misconfigured and non-functional model?

Error: 0x00554EE6

Problem: When trying to read information that a map model is controlled to appear at a certain time of day.
Solution: Some misconfigured "tobj" (time-controlled) object, but possibly even with uncontrolled objects.

Error: 0x0040AE08

Problem: The game tried to load a model that didn't exist or wasn't identified, related to the zone you are.
Solution: Problem with cargrp? pedgrp? Something bad configured?

Error: 0x004C4BB0

Problem: Related to unloading a model.
Solution: The "Backtrace" at the end of the log may have some indication, for example "0x0073A3A4 _ZN7CWeapon8ShutdownEv" indicates that it is related to a weapon (weapon.dat conflict?). It could be a problem with model settings (object, car, ped etc), .txd files etc.

Error: 0x00611C24

Problem: Get car model from cargrp.dat.
Solution: Incompatibility between the limit option of car models loaded in MixSets, and the cargrp limit of the fastman92 limit adjuster. Turn one off or wait for fixes.

Error: 0x007480DB

Problem: Related to playing the intro video (movies folder).
Solution: Some problem with the files in the movies folder, or other problem related to your PC or game not being able to play. A workaround is to use Improved Fastloader to skip videos.

Error: 0x006E0968

Problem: Related to siren turn on identification.
Solution: It was reported when using GPS Mod + Framerate Vigilante, and already fixed, download the new version of GPS Line Mod (from MixMods) to fix it.

Error: 0x00824844

Problem: Maybe related to rendering.
Solution: If there is "Direct3DCreate9Ex" right under the "0x00824844" in the "Backtrace" at the end of the log, it is probably caused by some model or graphic mod.

Error: 0x0041471F

Problem: Attempt to return collision between 2 points, a pointer was not sent to CColPoint.
Solution: This could be caused by some ASI or CLEO mod. Update the CJ Look Interest mod if you have it, it caused this problem when having NewOpcodes.cleo installed.

Error: 0x005DA66F

Problem: Rendering something from the game.
Solution: If there is "0x005D9F00" (CCustomCarEnvMapPipeline) right under the "0x005DA66F" in the "Backtrace" at the end of the log, it is probably caused by some vehicle mod. You can find out which one using the mod "Vehicles Test". Otherwise, it's something else related to game rendering, model mods, graphics...

Error: 0x004A9F54

Problem: Missing a special effect or some PRIM within the effect. Something removed from the .fxp file, or a .fxs removed from Effects Loader, which is needed by the game.
Solution: Identify, replace the necessary effects or backup the effects, if for example it was during an explosion it could be the explosion effect, or smoke etc. If you have "fxsfuncs.asi" in the Backtrace at the end of the log, it's probably an effect configured in FxsFuncs.ini.

Error: 0x005A329E

Problem: Related to procedural objects for surfaces.
Solution: It has already been caused by incompatibility between object.dat files, wrong object.dat or a bad merge of more than one object.dat in ModLoader. Identify and remove the wrong object.dat, or try mixing them manually with some difference checker tool.

Error: 0x004E516F
, 0x00693D75, 0x6F6C6C46
Problem: Related to pedestrian task.
Solution: It has been reported to use binaryipl.cs (a CLEO mod that loads all of the game's streaming .ipl files). Never use binaryipl.cs.

Error: 0x00405CBC

Problem: Not found LOD object in .ipl file.
Solution: Probably caused by a misconfigured .ipl file, or wrong mix between different mods that replaces same text and binary .ipl files ("stream"), some .ipl object doesn't exist etc. Identify the cause and remove such mod or try to fix it. The last file read from modloader.log can indicate which .ipl file it is.

Error: 0x0040AE92

Problem: Problem loading a car model from cargrp.dat.
Solution: The problem could be a misconfigured car in cargrp.dat or in fact the car is having problems loading and creating. Identify it, the Vehicles Test mod can help. Also reported when increasing cargrp limit in fastman92 limit adjuster with MinLoadedGangVeh in MixSets.

Error: 0x0040D349

Problem: Related to .txd streaming.
Solution: It has already been solved by increasing the streaming memory (StreamMemory in MixSets).

Error: 0x0053368B

Problem: Limit of PtrNode Doubles.
Solution: Use Open Limit Adjuster.

Error: 0x006FF35B

Problem: Something related to map objects that have road sign text.
Solution: It has already been caused by LOD Vegetation together with "LoadAllBinaryIPLs = 1" from Project2DFX or the same in Load Whole Map, or "binaryipl.cs". If you have more information, let us know.

Error: 0x00513347

Problem: The player no longer exists.
Solution: For some reason it was deleted or some deeper and weirder issue that caused this more serious problem.

Error: 0x00691238

Problem: Unable to get a person to perform a facial animation.
Solution: Most likely it was caused by some botched script that tried to make facial animation on a person who no longer exists. SCRLog can help you in this case. Otherwise it was some deeper problem, but related to this.

Error: 0x0156DA35
, 0x00470A65
Problem: Original game issue where the LOD connection of an object via script is not removed after the object is deleted, and remains in the saved game.
Solution: CLEO+ (v1.0.8 or newer) fixes the issue by both preventing and fixing saved games corrupted due to the issue.

Error: 0x007F06BD

Problem: Some problem when deleting some entity, be it an object, car etc.
Solution: One of the cases is a CLEO script that uses the CLEO+ CREATE_OBJECT_NO_SAVE command to create an object, but erases it with REMOVE_OBJECT_ELEGANTLY which is currently not supported. Use DELETE_OBJECT. If it wasn't caused by a script, it could be a problem with an object model or something.

Error: 0x006133DB

Problem: Some problem with pedgrp.dat/cargrp.dat.
Solution: Check your data/pedgrp.dat or cargrp.dat if it loaded correctly, if there is something wrong with ModLoader etc.

Error: 0x004C66CA

Problem: Tobj limit (timed objects) (time-controlled objects, defined in .ide).
Solution: Install Open Limit Adjuster, or increase the "timed objects" limit in fastman92 limit adjuster.

Error: 0x005380C3

Problem: Some problem loading models and IDs into .ide/.ipl.
Solution: Identify, fastman92 limit adjuster can even tell which ID, but basically it's some .ide/.ipl with missing or duplicate object.

Error: 0x0156680C
, 0x015667F0
Problem 1: Some bad script that worked with a non-existent vehicle.
Solution 1: Use SCRLog to find out which one.
Problem 2: main.scm/script.img incompatible with save game.
Solution 2: Use the correct and compatible files for the given game save, for example in full conversion mods etc.

Error: 0x0040F663

Problem: Something related to the collision model — .col files or its contents, some conflict, missing or something like that, usually map mods.
Solution: Identify which mod, whether or not it contains a .col file, contact the author or try to understand the problem further.

Error: 0x00604376

Problem: Something related to decision maker, probably some invalid decision maker value caused by some CLEO mod.
Solution: Try to identify by looking for CLEO mods that work with decision maker. This is a technical concept, so if you are a layman you will need a little luck, or help.

Error: 0x006D389B

Problem: Something related to installing tuning parts in a car. Apparently this is caused by a modloader issue when updating mods installed during the game and installing new tuning wheels.
Solution: If the problem is really with the modloader, the modloader itself needs to be corrected in a new version (reported in 0.3.7). Look for other ways to avoid this, but disabling auto mod update in the modloader menu is a good thing. If not, probably a problem with the model or installation of a tuning wheel.

Error: 0x00567187

Problem: Something related to collision models like .col files or even the vehicle collision model. Collision model could be wrong, missing, hit limits, something... Likely relationship with 417AAA?

Error: 0x00417AAA

Problem: Something related to collision models like .col files or even the vehicle collision model. The collision model may be wrong, missing, reached limits, something ... Probable relationship with 567187?

Error: 0x0073B6C3

Solution: Update CLEO+, the crash has been fixed.

Error: 0x00469FF7

Problem: There is a problem with a CLEO/SCM script. Probably a CLEO mod needs some ".cleo" that your game does not have installed.
Solution: The SCRLog mod can help you identify which script. Also check and install the necessary .cleo plugins for your scripts, such as CLEO+ or NewOpcodes.

Error: 0x0043EA2F

Problem: The game could not find an entrance/exit to an interior.
Solution: It has been reported saving the game inside an Enterable Hidden Interiors interior, and uninstalling the mod, so the game no longer has the interior and exit it was saved in and causes this crash.

Error: 0x0043EA2F

Problem: When clearing a list. It can be caused by many different reasons, other addresses in the "backtrace" can help.
Solution: It has been reported installing an .ipl file in text format replacing a binary (named "_stream"), which is wrong.

Error: 0x005D95CE

Problem: Related to clearing material list with effects, usually vehicles, but may not necessarily be caused by vehicle mods, this is a strange issue.
Solution: MixSets fix all crashes when closing the game.

Error: 0x00406036

Problem: Apparently some limit on .ipl files, or limit on the total content of all .ipls.
Solution: Remove some .ipl mods you have installed, or, if that is really the problem (it has been working without any .ipl), use fastman92 limit adjuster to increase the .ipl file limit, or merge them manually by copying the contents from one to the other, thus decreasing the number of .ipl files in your game. There's not much mystery, just be careful with the sections (eg all object lines need to be between "inst" to "end").

Error: 0x00749B7B

Problem: Trying to create a model that does not exist, or .txd does not exist. Or file name too long.
Solution 1: Check the installation of mods that need models, such as map objects. It has been reported trying to install a non-existent .dff or .txd into an .ide.
Solution 2: There was this issue in VehFuncs, fixed as of v2.0.8. Other mods that create models, probably any kind of model, can cause this, and probably just .asi, or the game itself tried to create a native game model that for some reason no longer exists.

Error: 0x0068FB5C

Problem: Related to the game's artificial intelligence tasks. What you specify are the addresses under the backtrace. If there is a "0x00681AAF" in the backtrace that is related to police patrol, it has already been reported in GTA Brasil, probably some third party mod that GTA Brasil uses, about AI and police.

Error: 0x0083D55B

Problem: Related to vehicle color settings. There are probably 2 mods that alter the operation or color limit of vehicles (carcols) causing conflict, or something else related to the color IDs.

Error: 0x0074E2BA

Problem: Related to some material of some model, like a car with buggy materials.
Solution: It has already been solved by simply identifying the car, (re) importing it into ZModeler and simply exporting it back. Probably ZModeler had exported the car with wrong materials and when importing back corrected them.

Error: 0x0070FB39

Problem: Could not find any vehicle's shadow model.
Solution: Identify the vehicle, contact the author, or correct it by checking if the shadow model is really present in dff and if it is working correctly. Disabling stencil shadows (those modeled, not low) will not crash, but it is not a real fix.

Error: 0x0046A220

Problem: Related to game script processing.
Solution: It could be something related to CLEO scripts, try to identify any CLEO mod that you have installed and caused a problem, but strangely it was also found to conflict with some mod (I don't know which) with SkyGfx.

Error: 0x00474BEF

Problem: Some cleo mod tried to get the pedtype from a non-existent ped.
Solution: As explained here, in this case you should use scrlog to find out which cleo script caused the error, and inform the author to fix it. One of the mods that causes this is the old version of GTA V XXX Service, fixed, if you use it, update it.

Error: 0x005FB2AA

Problem: A problem resetting groups, probably a game group limit.
Solution: It has already been reported using the Recruit More Members mod, now fixed, simply download the new version of the mod. If that's not your case, it's another mod (usually cleo) that works with groups and gangs.

Error: 0x00568642

Problem: Something related to a vehicle or object. It has been reported in an older version of Project Props where a fence model crashed on arrival.
Problem: If you use Project Props, please update it by downloading the new version as this problem has already been fixed. If you don't use it, find out which mod caused this and report.

Error: 0x007FDE84

Problem: Something related to the texture of some model. It could be .dff (where there is material asking for such a texture, so there is some request problem), or .txd (corrupted txd or something like that, probably less likely).

Error: 0x006B78DC

Problem: The game did not read the special handling settings for motorcycles or bicycles. It's a handling.cfg line that determines the cram etc. It could be caused by adding a motorcycle or bicycle without replacing and forgetting to add the special lines.
Solution: Try to identify the bike or bike with the problem, especially if it is added without replacing (which should be the reason for the problem), if it is added, check more carefully the tutorial to configure the fastman92 limit adjuster .ini file and the installation of handling lines. If it's not added, there could still be some problem about it, such as missing lines in handling, line with wrong name etc.

Error: 0x00418733

About: Could not read information on the collision model loaded from a vehicle, or object etc.
Problem: This occurred as a conflict when using ModLoader + SilentPatch + IndieVehicles + Advanced Aiming.
Solution: Update your IndieVehicles.asi, the problem has already been fixed. If it happens again, let me know there, threading the modloader log.

Error: 0x00657475

About: It has to do with pedestrian tasks, it could be something about boundaries, some cleo who works with pedestrians or something like that. There is more information here, if you find the solution or more information, it would be interesting to say there.

Error: 0x004C444A

About: With VehFuncs installed, in case this crash happens, the mod will give information about which vehicle model caused this.
About: When deleting a model, most likely a vehicle, but it can also be a pedestrian, a weapon, and in very rare cases, an object. If you have a "0x004089DD" under the backtrace, it really was during a model download.
Problem: It may have been caused by some model poorly made, poorly adapted, poorly modeled, it must be something internal to the model.
Solution: Identify which one, I recommend testing vehicles first and this mod can help. Uninstall and contact the author. Also remembering that it can be more than one model.

Error: 0x005334F0

About: It can be caused by several reasons. The address on the second line of "Backtrace" will help you understand the exact reason.
Problem 1: If you have a "0x005279B6" in the second line of Backtrace, it was caused by some mod related to the car camera.

Error: 0x0061006F

About: Random pedestrian loading in such zone of the map
Problem 1: Related to pedgrp.dat settings or some buggy pedestrian model.
Solution 1: Identify and uninstall such mods. Knowing the basics of how pedgrp.dat works you can determine which line or which pedestrian model you tried to load based on where you were at the time of the crash.

Error: 0x0072837D

Problem: Rendering a 2D sprite. It probably didn't exist.
Solution: One of the cases for this to happen is for example to use the more icons mod on the radar without the fastman92 limit adjuster installed or properly configured. It could be another similar case.

Error: 0x005FD56F

Problem: Related to the collision model (or simply the model or installation itself) of a gang pedestrian.
Solution: Try to identify a mod that changes gang models and uninstall, contact the author, etc.

Error: 0x005B6A70

Problem: Occurred while loading carcols.dat, when reading the colors of a line from it.
Solution: Identify which vehicle, which line, etc, and try to identify the problem or simply delete it. It was also reported to fix deleting gta_sa.set but it doesn't seem to make sense.

Error: 0x00681A94

Problem: Limit on some pedestrian's artificial intelligence tasks.
Solution: If you're not using Open Limit Adjuster, use it, if you're already using it, it's some sloppy cleo mod that does something with people (or rarely even with CJ itself).

Error: 0x005B6784

Problem: Related to invalid tuning parts; a bad configuration of the carmods of such a car.
Solution: Identify the car and try to correct its carmods configuration line by removing the parts that are incompatible with it.
Problem 2: A line of carmods configured with a non-existent car.
Solution 2: Identify the line, fix it; delete it.

Error: 0x004F1610
, 0x004EED28
About: It is common to happen in a "double crash" in modloader.log, thus appearing two crash dumps at the same time. You should use the crash that appears on top and COMPLETELY ignore this one, the correct one is the one that appeared on top of this one. In this case this would be considered a "false" crash. It is not known what started to cause this in people. If two didn't appear, well, this one has something to do with the game's audio.

Error: 0x005A3FA6

Problem: Related to procedural objects (configured by procobj.dat)
Solution: Identify which mod, or which object. Uninstall it, or uninstall any procobj.dat you have installed.

Error: 0x0074E36D

Problem: Related to some material of some model, probably a vehicle, and was probably saved incorrectly by ZModeler leaving the option "auto detect lights" checked at the time of export.
Solution: Identify which model, uninstall, inform the author, etc. It has already been fixed by simply reserving the vehicle in ZModeler by unchecking the "auto detect lights" option when exporting.

Error: 0x004AA8CB

Problem: You are missing the 'audio' folder. Or some important file inside it.
Solution: Check the audio folder and its files.

Error: 0x005A5C98

Problem: Clothes-related, more specifically in the texture of one, probably a .txd does not exist. This can happen when installing some player mod or clothing and trying to launch the save game with a non-compatible clothing.
Solution: Identify which .txd, and if clothing mod or player is your case, start a new game and see if it works. I recommend that you uninstall the mod, change the clothes from your saved game to the original ones from the beginning (or leave it naked), save the game again and reinstall the mod, it should work.

Error: 0x004AA614

Problem: Some bad configuration in effects.fxp.
Solution: Identify the problem or uninstall any effects.fxp that are installed etc.

Error: 0x006E3D9C

About: With VehFuncs installed, in case this crash happens, the mod will give information about which vehicle model caused this.
Problem: Incorrect animation group, possibly some line in vehicles.ide is wrong, either missing or misconfigured. For example, the number of the animation group on the handling.cfg line (the last number on the line) needs to match the name of the animation group (ifp) on the vehicles.ide line. If in doubt, simply use the values ​​that the game itself uses on the original cars, so you can't go wrong.
Solution: In addition to what was said above, in general check your cars and their respective lines of vehicles.ide, check if everything is ok, in general, manually or in the .txts with their lines installed in Mod Loader, also remembering that if you have a vehicles.ide inside Modloader, all .txts with lines from Vehicles will not load as stated in the Mod Loader tutorial. If even without such lines installed (or "even correctly installed") it still crashes, try to uninstall the cars in your game, you can use Test Car Load to test them and find the problem.

Error: 0x004EFE69

Problem: Problem initializing a sound. Possibly some sound that you modified has a problem or incompatibility.
Solution: This has already been reported when using the sounds that came with the G36C weapon. Uninstall these sounds, or other sounds you may have downloaded, trying to find out which one gave them.

Error: 0x00412144

Problem: Something collision model related (.col files).
Solution: Try to find out which mod edits or adds .col files and uninstall. Or try to identify the problem and try to fix the mod .col (may be related to spheres or boxes).

Error: 0x007F05E4

Problem: Some model, possibly a poorly modeled vehicle.
Solution: Has already been fixed after uninstalling such vehicle. It was a ROCAM lowpoly police motorcycle. It can happen with other vehicles, the problem is to be able to identify which one.

Error: 0x006F763F

Problem: Creating a train.
Solution: Has already been fixed after uninstalling Longer Trains mod. Did it also solve for you? Let me know.

Error: 0x00436686

Problem: Related to paths (car paths).
Solution: Remove mods that have some relationship to paths, such as mods that add new paths (new paths). There is a probability of being caused by the Traffic & Travel mod (extended version), if that was your case and it worked or not, (to be sure) Let me know!

Error: 0x007C91CC

Problem: Related to DirectX rendering in a skin (like a ped or possibly the player itself)
Solution 1: Uninstall the Normal Mapping by DK mod
Solution 2: If you do not solve with the solution above, then identify the skin mod you have installed and uninstall.

Error: 0x006E00C4
 (in Backtrace at end of log?)
Problem: Related to the position of a vehicle hitch.
Solution: It may be related to something like that, such as a hitch vehicle model (such as a tractor, truck, etc.). Even though it's strangely reported with the farm mod's countryCML.ide/.ipl files (which doesn't seem to make sense).

Error: 0x00454CC7

Solution: Leave "-1" or put a ; in the "PickupsDrawDist" function of MixSets (if you use it).

Error: 0x00756B89

Problem: Possibly some poorly modeled vehicle.

Error: 0x005DA63A

Problem: Related to vehicle pipeline, some mod that changes how the car graphics work, like SkyGfx (but not reported using it, apparently).

Error: 0x005A57EF

Problem: Two textures of different resolutions in player that need each other. For example if CJ's torso texture is 512x512, the shirt and tattoo texture also needs to be 512x512 etc.
Solution: Identify the mod, it could be that some player mod or costume is poorly made, or incompatibility if you have installed another costume, or if you are creating the costume, now you know how to solve it.

Error: 0x00441DB0

Problem: Something tried to catch the rotation of something and couldn't, probably some CLEO script.
Solution 1: If it was a CLEO mod, SCRLog can tell you exactly which script and which part of the script caused the problem. Probably some other CLEO mod deleted an important game object. If this happened in the Los Desperados mission ("riot2" script), I created a fix: https://sharemods.com/l0qzomu976ht/fix_riot2_object_door_crash.7z.html
Solution 2: Strangely it has been reported with some vehicle mods, but the exact reason is not known. The Vehicles Test mod can help you identify if that was it.

Error: 0x004AA2F4

Problem: Initialization of a special effect (fx / particle), as if you had initialized an effect that could not actually be created before.
Solution: It could have been some special effect mod you have installed. Identify; uninstall; warn us. It has already been reported with IMFX, probably bad installation of some effect (or lack thereof), such as headshot, where you have the option to simply open imfx.dat and disable the effects until you find it. It was reported in an old version of IMFX.

Error: 0x0156A2A7

Problem: Hit the script limit (CRunningScripts) (not .cs).
Solution: Use fastman92 limit adjuster. Look for "Running scripts" inside the .ini, remove the "#" at the beginning of the line and increase the number to like 200... or 300...... "Running scripts = 200".

Error: 0x0040AB3B

Problem: Empty data\pedgrp.dat line(s) or pedestrian name is wrong etc.
Solution: Check your file, back it up, uninstall one you have in Modloader etc.

Error: 0x007F3825

Problem: Unloading a texture. It has been reported after installing/uninstalling some vehicle without exiting the game using ModLoader (quite possibly any mod that includes texture?)
Solution: ModLoader has certain problems with this type of installation these days. It is best to avoid installing like this.

Error: 0x004D0C14

Problem: Related to animations (.ifp). Reported when selecting "Refresh modifications" in ModLoader menu.
Solution: Trying to identify which .ifp inside ModLoader was the cause?

Error: 0x0040AB3B

Problem: Empty data\pedgrp.dat line(s) or pedestrian name is wrong etc.
Solution: Check your file, back it up, uninstall one you have in Modloader etc.

Error: 0x004CEC60

Problem: Loading an .IFP file that does not exist or has the wrong internal name.
Solution: Check the installation of your mods that use .IFP, and the internal name of the IFP file (using some IFP editor, like Ryosuke839's GTA Anim Manager). The IFP's internal name appears at the top of the program when you open the IFP, and the name has to be the same as the filename.
Problem 2: Cannot find a required animation in .IFP
Solution 2: Some mod that needed some animation (usually .asi, not cleo) couldn't find it in .ifp. An example is you using the Run with Heavy Weapons mod with an incompatible ped.ifp.

Error: 0x007360ED

Problem: Related to guns/shots. It has been reported during a shootout at Madd Dogg's mansion. Possibly caused by Ryosuke's Bullet mod (version 2010, 2009 is not known) - as it was the only mod related to shots at the time.

Error: 0x00533606

Problem: Related to map boundary
Solution: Use Open Limit Adjuster

Error: 0x007FDE21

Problem: Related to textures of some model, whatever. The .txd may be having problems.
Solution: Try to find out which model caused the error, and open it in MagicTXD, possibly error messages might appear, try re-save, re-create .txd, re-place compressions etc to see if it fixes.

Error: 0x00533D6E

Problem: Creating some model. You can change the model type based on what is in the "backtrace" at the end of the log.
Solution: It has been reported using GTA III HD Vehicles Tri-Pack, where it occurs in Ocean Docks and is probably caused by some boat in the mod, but it could also be another vehicle.

Error: 0x00538103

Problem: Dummies (Dummy) limit for IPL.
Solution: Use Open Limit Adjuster.

Error: 0x007C51A8

Problem: Some pedestrian buggy.
Solution: Try to identify which pedestrian model, Skin Selector can help you with that.

Error: 0x00720089

About: World rendering.
Problem: The mod "24H Timecycle" is installed without the file "timecyc_24h.dat" being present in the "data" folder.
Solution 1: Uninstall the mod "24H Timecycle" or install "timecyc_24h.dat" in the "data" folder.

Error: 0x004C7D61

About: It is related to some vehicle node/frame memory corruption, however hard to say exactly what, it may be some vehicle you have installed that has some part causing corruption.

Error: 0x00571B73

Problem: There are over 400 different reasons... It won't be easy to find the reason with just this address. But know that it can be related to entities, physical things, like objects, people, cars. It can vary a lot, but in general it could be that the game tried to do something with something that no longer exists. It is possible for a CLEO mod including.

Error: 0x004C7DAD

About: With VehFuncs installed, the crash is automatically fixed and there will be information about the problem (such as which car caused it) in the VehFuncs.log.
Problem: In general the game could not find the wheel of any vehicle within its model. It could be caused by some weird internal problem in the game, or it could actually be a problem with modeling a car etc.

Error: 0x006DADBA
 0x006A6010
Problem: Some CLEO script or mission tried to take the RPM of a no longer existing vehicle. This is most likely, but strangely it has been reported to be some buggy model. It has been reported in a mission while using Improved SA Default Cars, missions using helicopter/airplane can crash it (and others?). It can cause on any vehicle you have downloaded if you don't use Improved SA Default Cars.
Solution: It's probably just a bug from some CLEO script or mission, or actually some vehicle was accidentally deleted from the game by another mod. If you use ISDC, try to find out which models gave this problem. It can also be caused by other vehicles you've downloaded that have buggy models, just find out which one, in the case of ISDC, was reported in Leviathan and during Marco's Bistro (which may have been caused by Shamal)

Error: 0x*
About:
 Vehicle license plate texture creation (present in vehicle.txd, but also changed by Improved Vehicle Features).
Backtrace: 0x006FDF15
Problem: Improved Vehicle Features mod error, apparently only present in v2.1.1 version.
Solution 1: Try using an old version, like v2.0.2, or reinstall the mod. If you are in the future and have released a newer version than v2.1.1, try using it.

Error: 0x0044F1C2

Problem: Paths, possibly the "nodes * .dat" files inside gta3.img.
Solution: Check them, backup them, remove mods that edit them etc.

Error: 0x0053388E
 or 0x0070FF4D
Problem: Possibly the game required more RAM memory than allowed.
Solution 1: Use Largeadress to increase the game's RAM recognition. This is the best and confirmed solution.
Solution 2: Decrease the memory usage (Stream Memory) by some mod like Mix Sets, lower it if it's high, a 1024 MB can fix.
Solution 3: Decrease your Project2DFX settings, avoid increasing the viewing distance of high quality models (if you have increased it), as you can decrease the game's overview distance in it too and this can also correct.
About: Also be sure to use SilentPatch to correct the artifacts that appear blinking on the map when reaching high RAM usage.

Error: 0x00757D6E

Problem: Problem with some model. It has already been reported during the Tuning Mod part selection, thus caused by such part...

Error: 0x00493E50

Problem: Searchlights. It has already been reported when using searchlight limit .asi mods, such as SAsearchlightlimitadjuster.asi.
Solution: If you use this .asi, stop using it. Use the Open Limit Adjuster in which it has the same function and nobody has problems with it, while these searchlights .asi several people have already reported problems.

Error: 0x00493E50

Problem: Searchlights. It has already been reported when using searchlight limit .asi mods, such as SAsearchlightlimitadjuster.asi.
Solution: If you use this .asi, stop using it. Use the Open Limit Adjuster in which it has the same function and nobody has problems with it, while these searchlights .asi several people have already reported problems.

Error: 0x007C4781

Problem: Some buggy vehicle, or something related to the game's animations.
Solution: Try to find out which vehicle gave the problem. The crash will only happen if that buggy car is loaded in the game, then closing the game will give this crash, so keep this in mind when trying to find out which of the vehicles caused this crash. Or it could be something weird about the animations. Most likely, simply installing MixSets (SkipShutdown function) will never again show the error message when closing the game, which may be a solution.

Error: 0x006BCAFE

Problem: Missing vehicle type special handling line.
Solution: In vehicles such as motorcycles, airplanes etc. there is a second line of handling that is necessary to function. You can see this line at the end of the handling.cfg file. Check that all necessary lines are installed for the vehicle to function.

Error: 0x007C4781

Problem: Processing a skin model. It has already been reported when opening parachutes with an edited model (like 90s AWP) having the game with high RAM usage.
Solution: This has been fixed when using Largeaddress

Error: 0x00564192
 (in Backtrace at end of log?). Or 0x00801D58 0x005D9802 0x005D97E6 0x00811A2A 0x006FA915 0x006129E1 0x007F3851 0x00552A53
Problem: Project2DFX 4.0 (0x00564192) or 3.2 (rest of addresses above). It may be corrected in the future, but it was reported in his TimedObjectsDrawDistance function.
Solution: Disable (by placing a "0.0") the TimedObjectsDrawDistance function inside SALodLights.ini. Or just ignore it by not closing the game via the menu.
0x006129E1 in "Backtrace": It's related to adding population to the map, so it might have something to do with it, with adding NPCs (any mod that handles this? popcycle.dat? NPC number increase? some mod that changes their model? ? apparently it was not possible to create an NPC).
0x007C4806 in "Backtrace": It's about downloading animation hierarchy, it may not be about animation but pedestrian skins. It is not possible to know exactly what happened, but it has already been reported with the mod Fix Male01, if it works for you, confirm us.

Error: 0x007C4781

Problem: Such issue has been reported when loading a save which has been saved outdoors (such as four dragons casino) and is using the HD Roadsignfont mod.
Solution: Don't use the mod or save game abroad. For example, uninstall the mod, open the save, save it inside and you can use HD Roadsignfont again.
Type 2: Crash at another time and without using the mod mentioned above?
Problem 2: This crash is related to the creation of "materials" (basically model textures). So it can be related to model mods.

Error: 0x00745393
, 0x0074533E
Problem: It has been reported when using HiDef Camera mod. After about 30 minutes playing? Using mods that use a lot of RAM like texture packs, cars etc?
Solution: Stop using it, avoid it, or use the Largeaddress mod (tested and fixed).

Error: 0x00650075

Problem: It has been reported when using Fixed Wayfarer mod.
Solution: For some reason the problem only happened to some people, so if you use this mod, simply uninstall it. If you don't use it, then it could be another .ifp/animation mod related to motorcycles.

Error: 0x004A981E

Problem: Has been reported when using Remastered Effects mod, and/or IMFX, and/or Combat FX.
About: Please give information if current versions the crash continues, or if you can reproduce the crash with as little as possible to say for sure exactly what is the exact way that this crash happens (for example if it happens only if IMFX is installed, something like that ) to give us information in order to try to understand how the crash happens and fix it. If you don't use these mods, well, be aware that it's related to downloading special effects, so it might be some mod like that.
Solution 1: It has already been said that removing "Explosion_satchel" from the Effects folder and disabling "explosions" in imfx.dat fixed this crash, please confirm.

Error: 0x004C672A

Problem: Limit of weapon models.
Solution: Read the tutorial on how to add new weapons, especially the "Weapon Models" part where you have to increase the weapons limit. Usually people don't pay attention to where it says about using Open Limit Adjuster along with this function. That is, if you use Open Limit Adjuster you do not need to activate the Weapon Models function of Fastman92 Limit Adjuster, otherwise it will crash.

Error: 0x0074EC24

Problem: Worldpipe.
Solution: SkyGfx edits it, so it was possibly caused by it, and in the .ini there is an option to disable Worldpipe, as was also explained in the readme. If you don't use SkyGfx then it could be another graphical mod like enb series or even textures.

Error: 0x00812152

Problem: Materials from some vehicle model. A vehicle part with poorly configured material probably. Probably need to increase the vehicle's special materials limit? MixSets has configuration for this and already increases by default, "CarMatPipeDataPool". Strangely it looks like it has already been fixed by changing the SkyGfx vehiclePipe from "Xbox" to another one, such as "Env".

Error: 0x00801D58
, 0x005D97E6, 0x005D9802. 0x00811A2A
Problem: Apparently related to Project2DFX.
Solution: Sent by Luiz Felip: If you want to continue using Project2DFX, you will have to go inside some place (mainly home) to leave the game or avoid leaving the game where you had the problem
(tested several times and apparently solved)
Click here for more detailed information.

Error: 0x00533620

Problem: Some model buggy.
Solution: It was already fixed when updating the mod "Vertex Color Fix". We don't know if it was caused by the same one posted on MixMods (here), if the one here is up to date, etc. If you had this problem and have downloaded it from here, let me know and try looking for another updated version. But if yours wasn't downloaded here, download Vertex Color Fix from here as it apparently is up to date.

Error: 0x005B8E6A

Problem: Stream Memory error, some mod that edits the game's stream memory may have entered some incorrect value.
Solution: This could be caused by an error in the Open Limit Adjuster, so you can disable or even delete the MemoryAvailable line from the limit_adjuster_gta3vcsa.ini. Also possibly you put some incorrect number in Mix Sets.ini in StreamMemoryMB function

Error: 0x0040ACD8

Problem: Wrong Cargrp.dat.
Solution: Sent and solved by Luiz Felipe: Back up the file, or check if the lines are correct or if they are not empty, possibly the error can happen when arriving in a certain place, for example, if it crashes when it arrives in the region of a beach or leaving the house on Praia de Santa Maria, it is apparently that the error comes from the line: "POPCYCLE_GROUP_BEACHFOLK"

Error: 0x00554751

Problem: Some model buggy. It was showing some big construction, that is, some big model like houses, stores, buildings in the place where you were. It has already been reported in Verdant Bluffs.
Solution: Try to find out, it could be anything related to that, try to go back to the same place where the crash occurred to be sure, or walk around that place. It can be caused by graphic mods like skygfx and enbseries as well as buggy models, possibly even textures, anything related to showing a large object on the map ...

Error: 0x004C4BD2

Problem: Some model buggy. It could be the lack of collision or something else related to it and the functioning of the model. According to Luiz Felipe, this problem happens when, for example, he renames the .dff and .txd of a car to the name of a pedestrian. Therefore, this crash can happen due to things like this, malfunctioning models, incorrect.
Solution: Check your models, it can be any type of model. Randomly case during the game can be mainly cars or peds; case in any part of the map, it is the model of the map that has collision with problems.

Error: 0x0058742D

Problem: Rendering the hud. It has been reported using a cleo mod called "Radar Zoom Fix".
Solution: If you use it, uninstall this mod, apparently it is totally the problem of the mod itself.

Error: 0x004946A4

Problem: Problem with some model. It has already been reported using Skybox from GTA V.

Error: 0x004C48D6

Problem 1: Ask for damage in the .dff of some car.
Problem 2: If it was in a Tuning Mod piece, it's a modeling error. The part hierarchy in ZModeler should only have one mesh, so attach everything, and leave the name with some unique name (don't use things like "chassis" in the name inside the .dff)
Solution 1/2: Attach everything. If there is still a problem, change the mesh name to something unique.
Problem 3: Crash in LV? INSANITY Vegetation.
Solution 3: So far (in Update 1.0) this crash is happening. Expect to fix or update your mod to the latest version.

Error: 0x004CAD9D

Problem 1: If you have "0x00733619" in the "Backtrace" (at the end of the log): Problem with some model / texture of some pedestrian, or mod that interferes with pedestrians.
Solution 1: Tag and remove.
About: If you don't have it in Backtrace, the problem may be another one, send the log saying.

Error: 0x0059BE3E

About: With VehFuncs installed, in case this crash happens, the mod will give information about which vehicle model caused this.
Problem: Modeling of some vehicle, most likely motorcycle, plane or pedestrian (slightly possible to be modeling of any other model). This has already been reported when installing a buggy Hydra, looking at the camera on it gave this crash.
Solution: Was it when looking at a vehicle? Identify which vehicle is buggy and uninstall. Test Car Load can help with that.

Error: 0x0F9491BB
, 0xAA94F20A, 0x91C9E7BF, 0x6449A5FF
Problem: Relationship with the crash below?

Error: 0x00718604

Problem: Reported problem on 90s AVP Reborn. As well as it can be some other vehicle pack. This appears to be an error caused by a very HD (with many polys) shadow model in .dff.
Solution: In the case of the 90s AVP, it was caused by the Super GT, that is, install another Super GT in its place. (again: The problem may not necessarily be this pack but any pack, or vehicle you have in your game.). You can use the Test Car Load mod to try to find the car. Just let the cars pass slowly and every car that is loaded you try to go to the Advanced menu to change the resolution, when it crashes, you'll know which car gave the problem). See if the problem with such vehicle is the very HD shadow model, which causes memory corruption due to overshooting game limits.

Error: 0x007EC9DA

Problem: ped.ifp missing.
Solution: Take a look at your "anim" folder, is ped.ifp there?

Error: 0x004AA3A1

Problem 1: Special effects (.fxp files). An effect could not be removed from memory due to an error.
Solution 1: Uninstall your changed effects
Problem 2: If you don't have special effects changed, it may be a problem with the model itself that uses some effect, such as a changed jetpack or some map object using 2dfx.
Solution 2: Identify and remove such a mod (.dff) that adds special effects. If you use Proper Fixes or Missing Smokes Fix, check them for updates.

Error: 0x0F9416FC

Problem: Save Game error related to save location
Solution: Sent by Luiz Felipe: Change the Save Game and avoid saving again in this same location (usually not saved by the original locations of the game, but through mods). You can also use save game editor programs to change the location where it was saved and this will correct your save.

Error: 0x006080BC

Problem: Some problem with some animation of ped.ifp
Solution: Uninstall any new installed ped.ifp or if you want you can try to mix .ifp files trying to solve without losing animations

Error: 0x6AC579A0
 (in "Backtrace" at the end of the log it will have 0x00507A6F)
Problem: Something related to sounds, be it your PC's sound drivers or sound packs.
Solution: If you have a sound pack, please uninstall it, if you can't try other kinds of things related to game sounds, like updating your sound drivers

Error: 0xE8AC1250
 (in "Backtrace" at the end of the log you will have several "unknown" and a shell32.dll)
Problem: Some kind of incompatibility from vehlightsfix.asi
Solution: Fixed increasing its priority in modloader.ini, ie put it in a folder and leave this folder at a high priority, like "100". Click here to learn how.

Error: 0x00406034
, 0x00406035, 0x00406038
Problem: Limits of .ipl files?
Solution: Fastman92 Limit Adjuster has function to increase the IPL limit, but there is a warning that this causes bugs. I recommend you try to mix the IPL files, taking for example 2 small IPLs, taking the objects from one and placing them in the other. Just don't overdo it as there is also a limit of objects within an IPL, but the limit is big.
The structure of an .ipl is basically like this:
urge
(all objects here)
end

Error: 0x006F3EF5

Problem: Limit of parked cars. The so-called "parked car generator".
Solution 1: Try to install Fastman92 Limit Adjuster, open the .ini and in "#Car generators = 500" remove the "#" (to activate the function), and increase the number to about 550, 600 or even more (if you have a fetish for parked cars).
Solution 2: Or simply decrease the parked cars, possibly you or mods have added too many parked cars on the map, even more poorly made cleo mods that each time you save the game it creates a new car, so it becomes a pile of parked cars in your save game, but in the new game or another save it will work, so you can take out such mods, and if it doesn't, you'll have to leave your save game behind and use another one like this.
Solution 3: Open the .ini of your Open Limit Adjuster and in "Vehicles" decrease the value in case above 200, leave between 110 and 200. It has already been solved in 130.

Error: 0x004C59CB

Problem: There is a problem when trying to get the model from memory.
Solution: It has been reported using the mod "Parachute always on the back". Uninstall it.

Error: 0x00746929

Problem: There are two GTA SA open at the same time.
Solution: Go to the Windows Task Manager, search for the game process and close all, then try to open it again.

Error: 0x007F05C0

Problem: Some poorly modeled car. There is little possibility of any other model like peds and objects, but it is usually cars.
Solution: Find out which car (or other model) and uninstall it from your game.

Error: 0x00679FA8

Problem: Add blood texture. It has been reported when using older versions of Enhanced Classic Graphics and IMFX.
Solution: Download the ECG or IMFX that this crash has been fixed

Error: 0x004C686D
 or 0x004C6637
Problem: "atomic models" limit, possibly limit adjusters conflict, like using Fastman92 Limit Adjuster with Open Limit Adjuster. Or it has reached the limit and needs to be increased.
Solution: In case of conflict, try putting a "#" at the beginning of the "AtomicModels" line inside the OLA .ini (limit_adjuster_gta3vcsa.ini). If you don't use any limit adjuster, install one (such as OLA) and the problem should be fixed.
Possibly then you will also have to follow the crash solution below:

Error: 0x004C675A

Problem: "clump models" limit, possibly limit adjusters conflict, such as using Fastman92 Limit Adjuster with Open Limit Adjuster.
Solution: Try putting a "#" at the beginning of the "ClumpModels" line inside the OLA .ini (limit_adjuster_gta3vcsa.ini)

Error: 0x007F39F0

Problem: Something related to finding textures in .txd, .txd probably could not be loaded because it was buggy.
Solution: It has already been reported in Freerunning Story 2.25 mod, you can look for which .txd specifically caused this and try to fix it by saving with Magic.TXD or uninstalling it.

Error: 0x0070BDAC

Problem: Low car shadow texture in particle.txd
Solution: Check your particle.txd, there might be a problem with the "shad_car" texture or anything else that didn't let this shadow work properly.

Error: 0x00804F51

Problem: Related to loading/unloading a model. It has been reported using 2 skin.img installed together in GTA (Skin Selector mod, which has even been updated without needing the .img)
Solution: If it was Skin Selector, check what was said above, or if you did something similar (like installing 2 identical .img etc, an error that usually happens to those who use Mod Loader and install wrong or twice accidentally)

Error: 0x0074C8C0

Problem: Relates to player clothing. It has already been reported for example in Amazing Player Female eyecat (cat eye) when trying to do one (or a few) missions.
Solution: Identify and do not wear such a piece of clothing on such a quest (or even in other cases).

Error: 0x004F1464

Problem: Problem with Steam's GTA SA audios.
Solution: Download and install the audio folder. Exactly which file was not reported, but if you can, all, or try to download at least from the radios. They were also told to delete the following files from the "steams" folder (even though I found it strange): ADVERTS, CH, CO, CR, DS, HC, MH, MR, NJ, RE, NJ TK

Error: 0x005D5CA2

Problem 1: (ImVehFt) Related to loading the dirt function on vehicles.
Solution 1: Possibly: Delete the gta_sa.set in your GTA folder and/or in the Documents/GTA San Andreas User Files folder, if not, check if the full address of the ImVehFt textures folder is less than 200 characters etc.
Problem 2: (you are not using ImVehFt) Related to loading the dirt function on vehicles.
Solution 2: Possibly you have added compression ("compressed") to the vehicle's dirt texture (or even other textures) inside models\generic\vehicle.txd, a common mistake people make for example when applying mipmapping to all textures automatically. Do not do this, such textures cannot contain "compressed".

Error: 0x015632B0

Problem: Hit limit of COL files
Solution 1: Make the COL files load by Mod Loader using a load line.
Place the .col in a folder inside the Modloader (for example "Modloader \ some folder \ test.col"), create a .txt in this same folder and inside the .txt place: "COLFILE 0 Modloader \ some folder \ test.col" , do this with all your .col files (they can all be in the same .txt). If you didn't understand, try to read the same thing explained in another way in the Mod Loader tutorial in the section "Installing COL files".
Solution 2: Use fastman92 limit adjuster to increase the COL limit on FILE_TYPE_COL.
Solution 3: Simply merge multiple .col files into one. With Coll Editor it is possible to simply open one and drag others to join them into one, thus reducing the amount of .col files in your game. Note that it may be necessary to increase other coll-related limits, but they are simple and usually Open Limit Adjuster solves them.

Error: 0x49646550
 (in the "Backtrace" at the end of the log will have "0x005A3FDE")
Solution 1: This is already resolved by removing Enterable Hidden Interiors.
Solution 2: This has already been resolved when using Crack 1.0 US Compact.
About: This crash can vary a lot, it can be caused by many different things.

Error: 0xE9F712A0
 (in the "Backtrace" at the end of the log it will have "0x00440973")
Problem: Car flashlight rendering.
Solution: Has already been fixed when uninstalling vehlightsfix.asi. Possibly there must have been some incompatibility with another mod.

Error: 0x6F746163
 (in the "Backtrace" at the end of the log will have "0x00440973")
Problem: Reload site map. It was reported after saving the game.
Solution: It has already been solved when saving the game to another location.

Error: 0x1BF1AFF3
, 0x03C03981, 0x03A53981, 0x03BD3576 (in the "Backtrace" at the end of the log will have "0x0040ED2B" or "0x00618ED6")
Problem: Trying to load model of some person or car dependent on the area you are in. This has already been reported when using Cop Bikers Overhaul and possibly a bad installation of the model, either dff/txd or the mod's own .ide. If you do not use this mod, same thing, it may be the lack of dff / txd or .ide badly configured thus missing a pedestrian and (rarely) vehicle, usually the crash happens in the absence of a pedestrian.
Solution: Submitted by Luiz Felipe: To fix this Cop Bikers Overhaul crash, simply DO NOT save the game outside the house, enter the game without this mod activated, save inside some house and install the mod normally again. If it still crashes, try another house.

Error: (in the "B
acktrace" at the end of the log will have "0x006E2BB7")
Solution: This is already fixed when using Crack 1.0 US Compact.

Error: (in the "B
acktrace" at the end of the log there will be "0x007FE8E7" and "SilentPatch.asi")
Problem: Incompatibility of old version of SilentPatch with Outfit mod (weapons by body)
Solution: Update your SilentPatch, the problem has already been fixed in new versions.

Error: 0x005D532A

Problem: Initialization of game scripts. It has already been reported when trying to start SAMP.
Solution: In SAMP, it was solved in one way, try: Run in administrator mode, either SAMP or GTA off; Possibly the problem was also in the save game, as well as water effect mods and overhaul cops.

Error: 0x004874EA

Problem: Some cleo mod. Look in your SCRLog.log (install it if you don't already have it and try playing it again)
Solution: According to AquaVXI, this has already been solved including uninstalling the Unofficial Patch smoke.dff/.txd and smokev.dff/.txd files.

Error: 0x00411160

Problem: It was while adding coll (.col) to the game. Possibly some incompatibility between mods? Something wrong with the .col.
Solution: It has already been reported when using: "PS2 Map + Fixes" + "Vertex Color Fix + 2DFX Effects" + "Farming Mod" (all together) and in this case the solution was to make the farm mod .col be loaded per line as shown in the "Installing COL files" section. Your problem might be similar, that is, some incompatibility, and you might fix it by making .COL be loaded this way, or by uninstalling such .col mods so as not to cause such incompatibility.

Error: 0x004C9239

Problem: Some problem with the handling line. Not installed? Wrong configured? Did you hit or miss setting the limit? Anything like that. More specifically the flags of the model.
Solution: Check in total, this crash has been reported when trying to add a car without replacing.

Error: 0x0064F8C3

Problem: Some .ifp file (from anims) is buggy; missing anims; badly converted etc.
Solution: Identify which .ifp is causing this and remove it. If it was right when you started the game, it was probably some ped.ifp you have installed.

Error: 0x004C9691

Problem 1: Any boundary conflicts? Are you using Fastman92 Limit Adjuster with multiple edited settings and Open Limit Adjuster together?
Solution 1: Try disabling (putting a "#" at the beginning of the line) the "AtomicModels" inside the Open Limit Adjuster .ini. Or if you are patient, try to find out which setting caused this problem in Fastman92 Limit Adjuster.
Problem 2: Was it a car you installed or are you modeling/editing?
Solution 2: In this case, it could be that the car was saved missing dummies, usually eg bump_front_ok. Or exported the .dff as "GTA 3" or "GTA VC" format instead of San Andreas. Keep an eye on the ZModeler export window etc. It could also be caused because you exported from ZModeler with non-visible parts.
Problem 3: SRT3 / RoSA Project (or maybe any other texture mod, or anything that uses .txd).
Solution 3: Read crash 0x00732924 or 0x00749B7B below:

Error: 0x004C9691
 0x00732924 0x00749B7B
Problem: SRT3 / RoSA Project (or maybe any other texture mod, or anything that uses .txd). Apparently caused by using non-power 2 textures in .txd. As taught in the Magic.TXD tutorial here on the blog, it is necessary that the textures resolution has a power number of 2, such as 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024, 2048, 4096 etc. .
Solution: If the crash was in the SF hospital, download the fix found here on MixMods in the SRT and/or RoSA Project post. If not in this location, let us know, if you don't use such mods then this is not the problem, but it can still be caused by another mod that modifies .txd, and is correctable by recreating the .txd (if you identify which .txd it gave the problem there) — exporting everything with txd workshop and recreating the .txd with magic txd. The solution may also be simply to change the resolution of the textures to power of 2, which in addition to correcting such a crash, corrects other visual bugs and improves the processing of the video card.
Problem 2: In the case of 0x00749B7B, get the models inside a model. It can happen for many reasons, such as some script trying to create a person whose model hasn't been loaded yet.
Solution 2: If you think this was caused by a script someone created, remove this script and contact the author, possibly the SCRLog.log will show which script caused the problem.
Problem 3: It could be due to a model (usually cars and skins?) being poorly adapted, converted, or saved in another GTA format (eg GTA VC format)
Solution 3: In this case, identify which model mod is giving this error (it will give the error when loading to appear in the game), uninstall, inform the author etc.
Problem 4: When loading the game after it has already loaded?
Solution 4: Disable the MixSets VehLODdist and/or DelayToRead function (DelayToRead seems to have fixed it and does virtually no harm to disable it). If it really does solve it and you're sure, I ask you to let me know so I can try to fix it.
Issue 5: It has been reported using mod "town_adjuster.asi", which is from Cops Bikers Overhaul. Apparently because I had the .asi installed without the .dff and .txd files from the police skins.
Solution 5: Reinstall the mod, make sure the cops .dff and .txd are actually loading, or simply delete the "town_adjuster.asi".

Error: 0x006A4523

Problem: When closing a car door, possibly non-existent.
Solution: If it was during Tuning Mod, be aware that in v1.5 or newer it has been fixed. If you weren't using the Tuning Mod, Scrlog.log will be able to tell you the problem (or not), it's very possible that it was some cleo mod that controls the car doors.

Error: 0x0045C7D4

Problem: This has been reported when using SkyGfx and trying to enable replay.
Solution: Do not activate, or if you accidentally press the key to activate replay, you can use MixSets by activating "DisaReplays"

Error: 0x00469FBC

Problem: Initialization of game scripts
Solution: Delete the folder "cleo\cleo_saves"
About: It is recommended not to save the game with too many cleos mods installed (or even other mods like maps). More information on taking care of the "health" of your save game HERE.

Error: 0x00822527

Problem: shopping.dat with errors.
Solution: Back up the shopping.dat, remove this file from the Mod Loader or replace it with the original in the Data folder.

Error: 0x004C8F24

Issue 1: This crash has been reported when using Stream Memory Fix 2.0, which is an extremely old and disused mod.
Solution 1: Stop using it and use MixSets and/or Open Limit Adjuster.
Problem 2: Some car limit problem.
Solution 2: Has already been fixed by installing Open Limit Adjuster.
Problem 3: Related to a car model.
Solution 3: Find and remove the car (if you can, notify the creator of the car). Test Car Load will help find the buggy car.

Error: 0x00532B82

Problem: Missing collider, most likely the game tried to create an object no longer installed in your game.
Solution: Check the installation of the mods you have, specially scripts with added models without replacing. RepairGTA can automatically remove all objects with unexistent model saved on you saved game, so fixing this crash.

Error: 0x00486726

Problem: Apparently hit the limit of models to be loaded at the same time by some cleo script.
Solution: You will need to remove some CLEO mods that create things like people, etc. This usually happens when starting the game when you have a lot of poorly made cleos mods (mods that load the models right when starting the game, which is a big mistake)

Error: 0x004CE15C

Problem: Error loading pedestrian animations. Possibly the "data\peds.ide" is misconfigured.
Solution: Fix the wrong line in peds.ide, thus correcting the animation placed on that pedestrian. If you don't know how to do this, ask the mod author. If you edited it yourself, review what you did better or go back up.

Error: 0x004CE15C

Problem: Error loading pedestrian animations. Possibly the "data\peds.ide" is misconfigured.
Solution: Fix the wrong line in peds.ide, thus correcting the animation placed on that pedestrian. If you don't know how to do this, ask the mod author. If you edited it yourself, review what you did better or go back up.

Error: 0x0057FAAD

Problem: Possibly caused by Widescreen Fix ...

Error: 0xC000007B

Problem: Missing some .dll, runtimes etc
Solution: Check the root folder of your GTA SA, if any .dll is missing there, a good tip is to copy all the .dll's from a backup GTA SA folder and paste in GTA with problem, but WITHOUT REPLACING so only paste the that are missing.
Solution 2: Click here to download the .dll's and runtimes that are possibly missing from your PC.

Error: 0x0054F3B3
, 0x0054F3B6
Problem: Probably some map mod (like adding objects), some map object mod, or some other strange problem ...

Error: 0x006FD525

Problem: Vehicle.txd, more specifically, car license plate textures. Also possible to be related to ImVehFt, board textures in ImVehFt\Plates folder.
Solution: Backup or install another mod that replaces Vehicle.txd or reinstall ImVehFt, there is a problem related to loading these textures.

Error: 0x0046504E

Problem: Related to some object, create, get it while it no longer exists, do something with it. Possibly caused by some badly done or poorly installed cleo script etc.

Error: 0x0059F8B4

Problem: Failed to load collision from .dff. The .col file is possibly not installed or the name inside the .COL file is different from the name of the .dff related to it, or there is simply no model .dff name inside the .COL
Solution: Check if there is a .COL file for the .dff properly installed and working in the game, as well as looking in modloader.log looking for if the .COL was loaded etc. Or check your .COL file to see if everything is in order.

Error: 0x00734E5A

Problem: TXD missing or incomplete or buggy or some mod tried to load some texture or some model that doesn't exist.

Error: 0x007F0875

Problem: Some poorly modeled car.
Solution: Find and remove the car (if you can, notify the creator of the car). Test Car Load will help find the buggy car.

Error: 0x006A65F6

Problem: Related to processing the suspension of a car, problem with its collision.
Solution: Look for which car has this problem and remove it, notify the creator.

Error: 0x0070BDAC

Solution: Disable HQ Shadows in .ini

Error: 0x0156CD5C

Problem: Related to script trying to "catch" someone. If the crash wasn't during a gang war, it's 100% sure it was caused by some cleo mod.
Solution 1: If the SCRLog is empty or ending in WAIT, then you must find which cleo gave the problem manually. Possibly it is some conflict or really bad mod, little is known about it.
Solution 2: It has already been solved by increasing the number of Vehicles in limit_adjuster_gta3vcsa.ini. Leave at least 110.
Solution 3: It was already solved when uninstalling the mod ManualDriveBy Remake.

Error: 0x00811A2A

Problem: Some vehicle reflection material.
Solution: Try to identify which vehicle, basically this type of error is: If the buggy car loads, when you close the game (or use load game?) it will crash, following that you can try to find out which was the buggy vehicle. Remembering that just entering the game and going to the street will load several cars referring to the place. The SkipShutdown function of MixSets removes the error message.

Error: 0x007C94E7

Problem: Some buggy model or graphic mod that messes with the models. Models of people/pedestrians.
Solution: Has already been fixed by removing Normal Map from DK22Pac while using Insanity Peds and Insanity Weapons Items. Remembering that using these mods without DK's Normal Map mod will work, but it won't have the effect of Normal Map. The same crash has already occurred in other mods that use Normal Map, even without having SkyGfx installed.

Error: 0x006E18F6

Problem: Texture of car flashlight light. It was reported when installing ImVehFt 2.0.2
Solution: Try to check if it is installed correctly, try not to use Mod Loader to install it, install it manually.

Error: 0x004082B1

Problem: Invalid handle / reference of a person from the script.
Solution: SCRLog can help you find out exactly which script caused the problem.

Error: 0x007C9119

Problem: Related to some problem with the functioning of a skin. It has already been reported using the Skin Selector mod or the always-on-the-back parachute mod along with Ryosuke839's Normal Mapping.
Solution: If you use Ryosuke's Normal Map, please uninstall it.

Error: 0x005A3280

Problem: Loading objects into object.dat file
Solution: Identify the mod and uninstall, or if you have 2 or more "object.dat" files in ModLoader, take the changes from one and put it in the other. This site can be helpful. There are several mods that use object.dat files, like Overdose Effects and some map mods like INSANITY Construction Site by Ezekiel.

Error: 0x006F7524

Problem: Starting train tracks, possibly problem with "tracks*.dat" files in data\paths folder

Error: 0x007FFF12

Problem: Get the image format (usually mods that load .png, .bmp images, etc.). This crash has been reported when trying to use ImVehFt on Windows 10
Solution: It was already fixed when reinstalling the mod folder, but the problem kept coming back.
Problem 2: Similar to the case above, such image (.png, .bmp etc) could not be loaded for some reason, including lack of it.
Solution 2: Identify and verify that mods that use images are correctly installed, for example the GTA V Hud.

Error: 0x006D867A

Problem: Wind speed. Possibly some mod that controls the game's wind? Like mods that edit rain or the Wind Mod created by me (if misconfiguring the .ini can cause this crash, I believe).

Error: 0x005725BF

Problem: Catch the distance between two zones (game areas such as neighborhoods)
Solution: Did you change any files that control anything about the zones? like .zon files or some other?

Error: 0x42480000
, 0x42480007, 0x42480008, 0x42480012 (in the "Backtrace" at the end of the log you will have 0x0056328C, otherwise, send it to us)
Problem 1: If there is any "0x0040E92F" in the "Backtrace" it was caused by some object in place. If you don't use ipl mods, map models etc but use some undownloaded GTA from MixMods, send the log explaining about it.
Issue 2: It was reported and fixed when updating Ginput (even though it doesn't make much sense).

Error: 0x004946A4

Problem: Reported when using GTA V Skybox
Solution: Remove it, very poorly done

Error: 0x00757D6E

Problem: Possibly some modeling of something (like a vehicle) or graphical mods (like enb series). It has already been reported selecting a part in Tuning Mod, so the problem is with that part.

Error: 0x007F5D85

Problem: Possibly some modeling of something (like a vehicle).

Error: 0x00611D99

Problem: Frequency of appearance of a vehicle
Solution: It's a number in the vehicles.ide line of that vehicle, click here to see which number, one of your cars must have this number configured wrong, check

Error: 0x00416C0B

Problem: Collision problem (collision model, coll) of something.

Error: 0x004AB7E7

Problem: Possibly some mod that messes with pedestrians / people or limit people in the game.
Solution: You can try removing some cleos mods that control people or using the Open Limit Adjuster.

Error: 0x00731C93

Problem: .TXD file limit
Solution: Download and install Fastman92 Limit Adjuster; Open fastman92limitAdjuster_GTASA.ini; In "FILE_TYPE_TXD" remove the "#" from the beginning of the line and increase the value. It can increase a lot, 500 or 1000 more.

Error: 0x0E0748C5
 or 0x0E3E9AD1 or 0x0FE75A1F (in the "Backtrace" at the end of the log will have 0x006A7770)
Problem: Reported when using do not blow up car while overturned mod (created by LINK/2012) (this mod is also included in MixSets)
Solution: Remove the mod, in the case of MixSets, disable the "VehFlpDontBurn" function within the Mix Sets.ini
Solution 2: Using NoDEP.asi may not help, but if it does, let me know!

Error: 0x08265E39
, 0x0E2656F3 (in the "Backtrace" at the end of the log will have 0x006ADB85)
Problem: Reported when using reverse gear mod together with MixSets, as MixSets already has this mod included (BrakeReverseFix inside .ini).
Solution: Delete the mod and leave only MixSets

Error: 0x00553927

Problem: When showing the LOD (low resolution model that appears far from the screen). This issue has been reported when using a spine mod.
Solution: Check your mods that change or add models etc, like trees or anything else that messes with the game's LODs or adds new models that don't have logs. As I say before, if you have any spine mods, delete it, it is poorly done and causes this crash.

Error: 0x006CAC47

Problem: Has been reported using Enhanced Functions with cars added without replacing.
Solution: Stop using Enhanced Functions, it's an obsolete mod, replaced by VehFuncs.

Error: 0x004AA134

Problem: Particle related (special effects)
Solution: Try removing your special effects mods. This issue has been reported when using a xenon mod (not xenon in cleo as it is just a cleo and does not change your game effects)

Error: 0x004F02D3

Problem: Related to playing a sound. It has been reported in SAMP when shooting close to someone
Solution: If you haven't changed your game sounds, it could be any other related issue, including your PC's audio drivers

Error: 0x004C53A6

About: Usually caused by some vehicle having the node name (basically, the name of the part) with a name that is too long (the limit is 23 characters, 25 or more causes serious problems in your game). With VehFuncs installed, this crash is automatically corrected. The information still remains in the .log in case you want to know which vehicle is causing the problem. Without VehFuncs, with or without this crash, the problem that leads to this crash also leads to other bugs and crashes in the game. More info here.

Error: 0x00571A10
, 0x00571A00
About: This can be caused by hundreds of different reasons.
Backtrace: 0x00490B77
Problem: Some mod applied too many tasks to the game's peds/NPCs, thus hitting the limit.
Solution 1: Identify and remove this mod cleo. You can use SCRLog for that, but basically it's some mod that controls NPCs. Notify the mod author to fix it.
Solution 2: Raise the task limit.

Error: 0x909090C3

Problem: This crash can happen due to several reasons, but it is usually caused by a conflict between 2 mods that used the game's system memory patch.

Error: 0x00536BE0

Problem: Getting the center of mass distance of a model.
Solution: If it was when creating a car, it is most likely the vehicle limit. You can increase the limit on "Vehicles" in the Open Limit Adjuster .ini file. By default it is "Vehicles = 110", try increasing it to "Vehicles = 500". If it was during normal gameplay, probably some botched CLEO mod is breaking the limit of vehicles created in your game, identify and remove.

Error: 0x005A5A47

Problem: Related to textures (from player.img?). This crash has already been reported when using mipmaps on player.img textures (CJ clothes etc)
Solution: Remove such edits, if you didn't do any of this, try to inform/find out what you did to give this problem too

Error: 0x00650311

Problem: Related to creating a random car driver (from the street)
Solution: ?... I had this crash myself and I still haven't found anything, if you had also help contributing

Error: 0x0040F64C

Problem: Possibly your special effects mods (effects.fxp)
Solution: Uninstall it. You can also try using the game's graphics at Low which may also fix the problem.

Error: 0x004F0E1C

Problem: Something related to sounds.
Solution: Are you using a sound pack? Try uninstalling it to see if it works.

Error: 0x0070AA31

Problem: Something related to the game's shadows.
Solution: If you are using shadow extender, you can try uninstalling it.

Error: 0x007F5A3A

Problem 1: If you have "0x006A2C29" in the "Backtrace" at the end of the log: Bad modeling of some vehicle.
Solution 1: Try to find out which vehicle and uninstall it.

Error: 0x006A65EF

Problem: Some vehicle without collision
Solution: Check your vehicles, if you don't know which one it is, test to see if they are working and stop looking for which one is faulty or manually uninstall, or all, some of them have .dff with errors. That should help you find.

Error: 0x0072837D

Problem: Related to on-screen sprites (anything added to the hud, images, texts)
Solution: Try to figure out which mod and delete it, be it any mod that added such things to the screen during the crash. This crash was reported with the possible cause: "Aviation Hud", confirm?

Error: 0x00405CB6

Problem: Lack of an IPL file or bad written IPL.
Solution: Check if there is any IPL missing to be loaded, either original from the game or one installed. Usually gta.dat files or in some readme come with IPL load lines inside, so reinstall such mods or delete them entirely.

Error: 0x00801D58

Problem: Usually some mods do give this error, I don't know why and which ones.

Error: 0x004C678E

Problem 1: Hit the vehicle model limit.
Solution 1: This crash has already been reported by the vehicle limit and was solved by using a Limit Adjuster, also checking if the Limit Adjuster is really working (they need some c++ visual, like Fastman92 Limit Adjuster)
Problem 2: Some vehicle model missing, wrong vehicle.ide, limit lines higher than necessary (usually caused by fastman92 limit adjuster misconfigured).
Solution 2: Check that your vehicle.ide is correct, not only it, but including lines of vehicles installed by Mod Loader. Also check that you have all vehicles installed in your GTA correctly and/or try to uninstall previously installed cars. If you use fastman92 limit adjuster, if the "Vehicle Models" setting is properly configured. Remember that if you use Open Limit Adjuster you must put a "#" at the beginning of this line in the fastman92 limit adjuster .ini, as the Open Limit Adjuster automatically configures it for you.

Error: 0x006FEC20
 or 0x0D3C1FA0 (0x006FECF5)
Problem: When rendering the text of traffic signs (those saying city names etc, roadsigntext).
Solution: Problem with the texture of the letters in particle.txd? did you use compression on this texture in particle.txd? Are you using .cs to increase the resolution of those cards? Some of these things may have caused the problem and you should of course check the particle.txd you are using, not adding compression ("compressed") to the roadsignfont texture, leaving Raster Raw.

Error: 0x004DD5A3

Problem 1: Missing "audio" folder
Solution 1: Your game is missing the "audio" folder, or the files are missing or corrupt.
Problem 2: Some mod that requires having full "audio" folder (not RIP).
Solution 2: Download the audio folder for GTA SA RIP. Or simply download the full game.
Problem 3: Something caused the audio driver to not be initialized.
Solution 3: Try to update and reinstall your PC's audio drivers. SilentPatch also fixes some incompatibilities with audio drivers.

Error: 0x004D3FBC

Problem: Did you try to use an animation from an unloaded IFP? IFP buggy and cannot be loaded by game?

Error: 0x0065ED19

Solution: This crash has already been solved by cleaning the Mod Loader folder, removing unnecessary files. But I believe this doesn't make sense and it wasn't really because of that

Error: 0x0048C3A9

Problem: Error trying to load an IFP. Quite possibly the IFP is not installed on your GTA.
Solution: Check the installation of the IFPs. In SCRLog.log it should have the name of the script in which you requested the IFP

Error: 0x0057A065

Problem 1: It has already been reported when using buggy car. Reported with mod 90s AVP because of Bandito, where after spawning him and going to display menu, it will crash.
Solution 1: Replace the car with one which does not have this bug.
Problem 2: For some reason it was not possible to identify the video mode.
Solution 2: This has already been reported and simply stopped giving the error, by itself, or some mod that made it impossible. You can also try deleting gta_sa.set in "Documents/GTA San Andreas User Files".
About: If you use 90s AVP Reborn, also read crash 718604

Error: 0x006BF73B

Problem: Related to the collision model of some bike, however this can be caused by other factors such as limits being hit.

Error: 0x006999EF

Problem: Related to objects (from poles, fire hydrants to doors and other objects controlled by script), apparently some problem when processing the list of these objects. To do with Save Game? Bugged object?

Error: 0x004C4576

Problem 1: When trying to load tuning parts from carmods.dat. This crash has also been reported when trying to reload cars in-game via modloader.
Solution 1: Check your parts and/or carmods.dat, it could be that you accidentally deleted some tuning part model, bad configuration of some car line etc.
Problem 2: The data/gta.dat file is missing.
Solution 2: Make sure it's there.

Error: 0x0071A190

Problem: Font (letters), probably some fonts.dat or corrupted letters from some mod (.fxt) or translation (.gxt).
Solution: It has already been solved by uninstalling the translation, but it does not always happen, try to identify the cause, exactly which text, if it is a conflict, etc.

Error: 0x006F32C0

Problem: Reported when trying to add a parked car with a model of a car added (i.e. non-native to the game, a car installed without replacing). Or some limit or corruption related to parked cars.
Solution 1: To be able to park cars added in the game without replacing, it is necessary to open the Fastman92 Limit Adjuster .ini, search for the line "#Accept any ID for car generator = 0" remove the # and put = 1.
Solution 2: Use RepairGTA mod to fix duplicate and incorrect cars in your game.

Error: 0x005A5781

Problem: Related to copying textures. Apparently there is a texture with compression, and GTA didn't support compression on it. This crash has been reported when compressing the "vehiclegrunge256" texture of vehicle.txd without having ImVehFt installed.
Solution: Try to find out which .txd has this crash, uninstall it or open it with TXD Workshop, double click on that texture marked "Compressed" (there may be several, or all) and disable its "Compressed" , save the TXD and try again (if it solves etc, report to the author).

Error: 0x00537D12

Problem: Hit the model limit inside a COL file
Solution: Use Open Limit Adjuster

Error: 0x00632D15

Problem: Related to placing an animation sequence on an actor
Solution 1: Any cleo scripts? see in SCRLog.log
Solution 2: Possibly some other mod (usually cleo) removed that person and so the game crashed when trying to add animation on someone non-existent. Try to manually find out which mod did this, as in these cases SCRLog.log shouldn't help.

Error: 0x00668269

Problem: Related to making someone walk and stop somewhere
Solution 1: Any cleo scripts? see in SCRLog.log
Solution 2: Possibly some other mod (usually cleo) removed that person and so the game crashed when trying to add animation on someone non-existent. Try to manually find out which mod did this, as in these cases SCRLog.log shouldn't help.

Error: 0x006EB670

Problem: Problem when trying to start the game water, possibly a problem with the "waterwake" texture of "models \ particle.txd"
Solution: Check this texture, or other textures related to water

Error: 0x006B4220

Problem: Processing a person's death. This type of crash is common and difficult to understand the reason for this, if you have already managed to solve such a thing, let me know. It's complicated because it usually happens randomly, so it's hard to know if you've fixed it or not. But I believe it might have to do with some poorly made mod cleo that controls people.

Error: 0x007F0C41

Problem: Related to some vehicle model (or in a certain case, construction of CJ's clothing)
Solution: It has already been reported as incompatibility of SkyGfx with another mod. See if this is your case and identify the mod and update SkyGfx to the new version. But it's probably some strange problem with models, usually vehicles.

Error: 0x004D68BA

Problem 1: It is related to the processing of animations. If you have 0x006BB8B0 in Backtrace at the end of the log, then it is related to a motorcycle animation.
Solution 1: It has already been reported to run VERY fast, maybe the speed caused an error. It can also be anything else related to motorcycle animations.

Error: 0x49646550
 or 0x42480000 (but what matters is that the backtrace at the end of the log will have 0x004091E2 or 0x005641D2)
Problem: After loading the game after loading the first one or the CJ dying or closing the game? And have you previously installed/uninstalled any in-game map mod via ModLoader?
Solution: So far, ModLoader has some installation problems within the game. The crash has already been reported when installing/uninstalling mods GTA IV Light poles, New poles in HD and there must be others of the same type.

Error: 0x00544BC8
 or 0x00542721, also possibly 0x00542830
Problem: Vehicle limit in the pool, or physical entities (which includes vehicles among other physical things)
Solution: Download and install the Open Limit Adjuster, if you have already installed it and continue the errors, go to the OLA .ini, if the "EntryInfoNode" function is disabled, activate it by removing the "#" and leave "unlimited"
Solution 2: (Luiz Felipe) If you are already using the Open Limit Adjuster and this crash happens when using the explode all vehicles cheat (CPKTNWT), go to OLA's .ini, look for the "EntryInfoNode" function, remove the "= unlimited " and put "=750" (or more). If you're using map mods that add models or the like, leave "= 1500" to be safe.

Error: 0x0059FE47

Problem: In pre-rendering an object, after adding the size to it, I don't know if it was because of the size, but GTA has an original crash where it makes the game crash if you move the camera against a script-edited size object . This crash has already been reported when dying with the Ground Weapon mod.
Solution: Find out where the crash occurs, possibly the object is stuck on the game's map, so in a new game or other save game it won't crash, the problem is stuck in your save game (read more here). If not, some script must have created an object there that made this crash, find out which script.

Error: 0x0072F4DE

Problem: Related to memory allocation. This crash has already been reported by a buggy car, but it's a very generic problem, may be a lot of different cases, the backtrace can tell more information. Contact someone experienced.

Error: 0x0040890A

Problem: Some CLEO mod tried to load an existing model.
Solution: The SCRLog mod can tell you exactly which script caused the problem. Make sure the mod is correctly and completely installed.

Error: 0x004C663B

Problem: Hit the game's object limit. It's a crash that happens when installing too many new objects or too many Tuning Mod pieces.
Solution: Use Open Limit Adjuster

Error: 0x0040FB80

Problem: Collision related (coll), possibly hitting the game's collision limit, or other issue about .col.
Solution 1: Use Open Limit Adjuster?
Solution 2: It has already been fixed due to some bad configuration of fastman92 limit adjuster.
Solution 3: If you are trying to start SAMP, probably samp.exe has a different compatibility mode than gta_sa.exe, or some other reason why SAMP cannot open gta_sa.exe (bad configuration, there is already some gta_sa. exe in Task Manager, some program preventing startup (you can try restarting the PC) etc).

Error: 0x004C67BB

Problem: Limit of pedestrian models in .ide
Solution: Use Open Limit Adjuster

Error: 0x006D1080

Problem: Failure to handle a vehicle, quite possibly the vehicle disappeared from the game and some bad mod ended up trying to handle a non-existent car
Solution: Possibly it was a cleo and possibly won't generate SCRLog.log for you to know which cleo... you will have to look for which script manually gave this error, unfortunately. If it was a MixMods mod, let me know.

Error: 0x005B6B2F

Problem 1: Two identical IDs being used in data / vehicles.ide
Solution 1: Check your vehicles.ide or lines of it, must have duplicate line or id already used etc, things like that. It can even be a line with a badly configured model, missing etc.
Problem 2: Error in carcols.dat, number of color variations, possibly some car has more than 16 colors in its carcols line or vehicles.ide is misconfigured.
Solution 2: Delete the number of color variations of the car to make it less than 16, or use some mod that increases the limit of color variations. It is also possible that you installed the colors in the wrong places, placing the lines of 2 colors where they are for 4 or vice versa, if you do not know, install by Mod Loader, it will install the lines correctly for you.
The problem can also be because of the badly configured vehicles.ide, review the models and IDs if they are all correct etc.

Error: 0x00563289

About: With VehFuncs installed, in case this crash happens, the mod will give information about which vehicle model caused this. However, this particular crash is usually not about cars.
Problem1: Error removing an object from the map, possibly an object stuck in the save game
Solution 1: Try to see if another save game or new game doesn't crash at that location, if it didn't, then you must have saved the game with some script mod that adds an object to the map. Click here to download a mod that will enable you to fix this crash, just look for the bugger object on the spot and delete it. Or click here to download a new save game and see some tips.
Problem2: It can also be any type of model, such as poorly made vehicles (there is still a slight possibility of being skins and clothes).
Solution2: Try to uninstall all your vehicles or try to find which one. If the crash is while you are playing, try using Test Car Load to find out which of the vehicles caused the problem.
Problem3: Any necessary mods (object related?) are missing from your game. Possibly you will have this problem only in a save, and right after uninstalling some mods.
Solution 3: Replace the mod you uninstalled, possibly the game needs it.

Error: 0x004A2CF3

Problem: Related to special effects, you probably have an effect (.fxp or .fxs) installed but you are using an unsupported "effectsPC.txd" without any texture there.
Solution: Check your .fxp and effectsPC.txd files in modloader, it might be conflict.

Error: 0x007F120E

Problem: Frame not found. It can be caused by about 40 reasons like buggy model or script controlling something most likely from a car (but it could still be a weapon or a person). This also happens in MixSets version 4.0.5 or older when blowing up too many cars, it has been fixed in the new versions. If you have "0x005670AB" in the Backtrace just below, it is caused by dropping a part from a car.
Solution: If you use MixSets 4.0.5 or older, update it as this crash has been fixed. It has already been reported when trying to tune a car unprepared for tuning. Possibly the crash can also happen when approaching a garage with a car with unsupported tuning parts inside. Check your mods and models. In case of a crash due to some tuning in a car that doesn't have support, simply don't tune or try to configure his carmods.dat line correctly because apparently the lines are incorrect. It has also been reported when using the Windshield Removal mod, on motorcycles, which did not have a windshield (as can any other type of mod that removes vehicle parts)

Error: 0x004D41C5

Problem: Problem with the animation of getting into a vehicle, it could have been you or someone on the street (if the crash was during the game without you getting into one)
Solution: Try to find out which vehicle (if you don't know) and check the vehicle.ide and/or .ifp lines (if you edited an .ifp, it may lack some animation). This crash has even been reported when using the F-14 plane, but apparently due to a problem with the plane itself, where you need to enter it from the right side otherwise this crash occurs here.

Error: 0x007F3737

Problem: Loading textures from a TXD (any TXDs having a problem?)
Solution: Check your TXD

Error: 0x006F785F

Problem: Creating a train. It has been reported using multiple train-related script mods at the same time.
Solution: Uninstall some CLEO train mods, avoid using multiple train script mods at the same time. It may be that other mods of the type also cause such problems, as I said, creating a train, if someone messes with train creations, it could be a conflict.

Error: 0x004F1464

Problem: Related to loading some music (division by 0)
Solution: Remove songs if you added any? Bad edition of GTA SA RIP? Did the game come buggy? If you have crashes in missions even without mods, it may be your GTA that is buggy, you need to download another one (download GTA SA from here). In the case of the Steam GTA, it has been reported to do a bad downgrade (without using the downgrade tool).

Error: 0x007F39FB

Problem 1: You have an .img file open.
Solution 1: Close it.
Problem 2: Loading a texture (inside TXD). Apparently an original ModLoader bug having a hud.txd installed on it. It can happen when starting the game, and next time it works.
Solution 2: Delete all hud.txd that are installed inside ModLoader. If you have more than 1, try to uninstall and leave only 1 of them.
Problem 3: Failed to load any clothing .txd or vehicle.txd. Or else some paintjob from a car.
Problem 4: Some CLEO script tried to load a sprite texture into some .txd ("models/txd") but didn't load the .txd file before. For example in an old version of ATP.
Solution 4: Identify the mod CLEO, note that the .txd file may even exist (if the .txd file does not exist but CLEO tries to load, the problem is another one), the problem may be directly as an error of some CLEO mod that need .txd but forgot to load it.
About: It could be anything related to "loading a texture from a .txd file", so it could be caused by hundreds of different reasons, but one thing is certain: There's some .txd wrong there, possibly buggy or missing some important texture, things like that.

Error: 0x00745AA5

Problem 1: It has already been reported when using buggy car. Reported with mod 90s AVP because of Bandito, where after spawning him and going to display menu, it will crash.
Solution 1: Replace the car with one which does not have this bug.
Problem 2: For some reason it was not possible to identify the video mode.
Solution 2: This has already been reported and simply stopped giving the error, by itself, or some mod that made it impossible. You can also try deleting gta_sa.set in "Documents/GTA San Andreas User Files".

Error: 0x005FD54D

Problem: Creating a pedestrian.
Solution: Find which of the pedestrian skins has a problem and remove it. If you want, contact her creator. Strangely it has already been solved because it is incompatible with Trees Remove + Left 4 Theft.

Error: 0x0074A4C0
 or 0x0074A4C4
Problem: Removing a 3D entity, quite possibly Tuning Mod crash on part selection after installing a wrong or buggy part
Solution: If it was a part, remove it, contact its creator or check its installation. Saying what the piece was here in the comments should also help

Error: 0x004D464E

Problem: Animation problem in some animgroup, either weapons or walking styles.
Solution: Could have been caused by editing weapon.dat changing the weapon's .ifp file, but not also changing the default.ide file (which is the file where the weapon and its .ifp is loaded). Just as it may have been caused by a script that tried to put the gun on someone, but the gun was not loaded, and so will this crash. The same error can be caused by a misconfigured animgroup in the ifp part (animgrp.dat). It is best to identify which mod is giving this (following the details I just said) and contact the author of this mod to fix it by having the necessary .ifp file loaded for that weapon (or the weapon itself is loaded) in game memory).
Problem 2: A new line of weapon.dat without having fastman92 limit adjuster installed and configured.
Solution 2: If this is your case, identify, check if you have any weapon lines installed (either weapon.dat or .txt files containing lines from it), remove or install fastman92 limit adjuster, configure it correctly etc.

Error: 0x0080D5EF

Problem: Transforming a 3D point
Solution: It may or may not be reasons for car models or explosion systems of some mod (usually asi). Try starting the game in admin mode and with Windows XP SP3 compatibility (this has already solved one person's problem)

Error: 0x00405CA4

Problem: Error with binary IPLs. Wrong ID.
Solution: Fix or remove (if new) your binary IPLs (inside .img or Modloader)

Error: 0x0053C1F5
 or 0x0053E986
Problem: Missing NewOpcodes.cleo? Some mod ask for it and you don't have it?
About: Try downloading it and installing it in your cleo folder.

Error: 0x007F18CF

Problem: Related to a matrix, possibly a model.
In the Backtrace at the bottom, if it has a 0x004AAFCC, 0x0053C1F5 and/or 0x0053E986 is related to special particles/effects (there are other possibilities to be too). Otherwise, or having 0x0080981D, it may simply be about a 3D model. In the case of 0x008095FA it could also be some model, but it was reported when trying to delete an object (in the test, a tree) using the 09A2 opcode, ie it could be a CLEO that tried to delete an object from the game, but this can also happen rarely in a mod asi.
Solution: It has already been reported due to a poorly made car, just identify and uninstall the car, Vehicles Test can help.

Error: 0x004F0E67

Problem: Possibly sound problem from your PC, DirectPlay, or is using Mobile sounds mod.
Solution: Read Error: DSOUND.dll
 (ctrl+f)

Error: 0x004AA4C8

Problem: Special effect (effects.fxp) not found or missing.
Solution: Check your effects.fxp, possibly you replaced it with one that is missing an effect or you are using some mod that uses an effect that is missing inside your effects.fxp.

Error: 0x00705D48

Problem: Related to the processing of dynamic shadows.
Solution: Uninstall any mod that messes with them, or disable them with MixSets or SkyGfx, or simply leave the game at Low setting.

Error: 0x00826360

Problem: When trying to read some text, the text did not exist. It could be for several reasons.
Solution: Invalid timecyc.dat file, it happens because there is some error (for example, some line is missing) in your timecyc.dat or you are using the mod Timecycle 24H with some timecyc.dat installed in the modloader (just uninstall the timecyc.dat from the modloader ).

Error: 0x008214E4

Problem: Error trying to load some handling line. Possibly your handling.cfg is wrong or any handling lines installed in your game may have some problem which caused them not to be read.
Solution: Check the lines, uninstall them to see if they fix or anything.

Error: 0x007F0BF7

Problem: Frame did not find the child, it usually occurs when trying to install a tuning part in a vehicle in which it does not support it.
Solution: If the car was downloaded, check the installation of the carmods.dat line or avoid tuning it. If the crash was near a garage in a house, it means that the car previously saved there has parts that your current (replaced) car does not support, return your game to its previous state (with the same car model in which it was saved in garage) or edit your save game to remove cars from it, or avoid passing near this garage.

Error: 0x004082C0

Problem: Possibly the save game is not compatible with your .exe or main.scm
Solution: If the save was not made for Crack 1.0 US, I recommend downloading another save. Also try clicking here and downloading the original main.scm.

Error: 0x004C720C

Problem: This has already been reported with Tuning Mod v2.
Solution: If you use Tuning Mod v2, know that the problem has already been fixed in v2.1. You can also re-download the updated IndieVehHandlings.cs with the fix.

Error: 0x004C7170

Problem: This has been reported with Tuning Mod v2, usually right after
Solution: If you use Tuning Mod v2, know that the problem has already been fixed in v2.1. You can also re-download the updated IndieVehHandlings.cs with the fix.

Error: 0x005381A5

Problem 1: Incorrect IPL or buggy model (crash when trying to load a stanza from an IPL). By reports, this also has to do with mods and saved game
Solution 1: Check the IPLs or models. If the problem is no save, try using Delete Objects
Issue 2: It has been reported using Open Limit Adjuster not configured for Project2dfx.
Solution 2: In case, Project2dfx comes with an Open Limit Adjuster properly configured for it, you need to use it, remove another Open Limit Adjuster from your GTA (if you have two) and leave Project 2DFX's own.

Error: 0x00465CC8

Problem 1: A script tried to add a task to some non-existent actor.
Solution 1: Possibly a cleo script, try to identify it. SCRLog.log can help with this.
Problem 2: Used Skin Selector while using DYOM.
Solution 2: Don't use.

Error: 0x00553F71

Problem: Related to map rendering.

Error: 0x00534134

Problem 1: The same ID being loaded on different models, very common in installing different map mods with authors who don't care about compatibility. If you had this crash after installing a part in Tuning Mod, it is because two parts (or some other different mod) are using the same ID, inform the author and/or follow this tutorial to fix the incompatibility.
Solution 1: Review your new IDE files, one might be using the same ID as the other. In most mods (not scripts) you can just open and change the id to some free one (click here for list or use this tutorial to fix the incompatibility).
Problem 2: Inappropriate (or missing) COL
Solution 2: COL: Review whether the COL is being loaded on the IMG or Mod Loader, if IMG, also review whether the IMG is being loaded on gta.dat or Mod Loader. To install a COL in Mod Loader correctly, follow the Mod Loader Tutorial in the part where it talks about installing .COL
Problem 3: Object with LOD was removed.
Solution 3: Remove a map object that contains LOD, it is necessary to use both the *_stream*.ipl file (inside gta3.img) and the .ipl file from the data/maps folder. If you for example remove an object only in the *_stream*.ipl file but not also remove it from the .ipl from the data/maps folder, it will cause this crash. What can also happen when installing a mod, for example you already have a mod that changes the same .ipl file, so the necessary file will not be loaded and will cause this crash. You will have to check that the files are all installed and loading (you can check modloader.log to see if it is loading, if you already have another file installed etc). Alternatively, if you're creating a map mod, you can move the object underground instead of deleting it, so you'll avoid problems like this but you'll also have to do the same with the LOD (which is in the .ipl of the data folder / maps).
Problem 4: You have some game .img open in some program, like Alci's IMG Editor.
Solution 4: Close it.

Error: 0x0040E179

Type: The game freezes when looking at an object
Problem: TXD (or other feature (except DFF)?) is not present in IMG.
Solution: Add the TXD to the IMG or remove the IDE/IPL from the related object.

Error: 0x005B51F7

Problem: Related to IPL and its connections between normal objects and LODs. Some IDE is missing. Possibly the loading lines are not installed or the .IDE file is misspelled, or the link between the common object and LOD is wrong.
Solution: Fix gta.dat or check if gta.dat or load line is present inside Mod Loader. Also check that the .IDE file related to such .IPL is correctly configured with the necessary objects for the .IPL within the "objs...end" section.

Error: 0x005BA12B

Problem: Broken IPL resort limit (1000) - Maximum lines in "inst" section inside some IPL file.
Solution: Increase the IPL resort limit with some Limit Adjuster or try to split one IPL into others.

Error: 0x005DC425

Problem 1: Incorrect collision material (Inappropriate material ID).
Solution 1: Fix the material ID within the COL file. A tip is, after you identify exactly which model and which .col file is causing the problem, open the .col in Coll Editor, select the model with the problem, or that you think has the problem, go to Edit Mode, in Face, and Select All to select all, and see in "Material" the number that appears. If you just created the .col then everything will probably be "0", which is the default, but if you have any invalid IDs, it will be with another bug number and so will not show any numbers there. Changing the Material to 0 with all faces selected will change everything to 0, including the bug face, and fix the problem. This is probably caused by Coll Editor merging different .col files, probably some Coll Editor bug.
Problem 2: Strangely, a timecycle related issue (timecyc.dat).
Solution 2: It happened in the "lite" version of Real Linear Graphics, it has already been fixed. Strangely, the solution was to lower the intensity value of the 7 pm line of the San Fierro fog climate, as the crash was in Los Santos, it is not known for sure how this happened.

Error: 0x006E9248

Problem: Water related (incorrect water.dat?) (in water rendering). Division by 0.
Solution: Fix the water.dat.

Error: 0x006F5702

Problem: Too many objects? Some unknown boundary.

Error: 0x007ECABB

Stack: 0x4CDCDE > Error
Problem: Corrupt texture format (problem with low resolution textures). This could be caused by the WTD2TXD tool.
Solution: Fix the TXD. Check if low resolution textures are marked with compression (compressed, DXT).

Error: 0x00000000

Problem: Some CLEO/SCM script.
Solution: Use SCRLog.log to find out which





SCRLOG


By commands:

Last command: [0001] WAIT
Problem: The problem is you. Read the SCRLOG page better, it was already talking about [0001].

Last Command: (Some Bitwise): [0B10] or [0B11] or [0B12] or [0B13] or [0B14] or [0B15] or [0B16] | (Some .ini): [0AF0] or [0AF1] or [0AF2] or [0AF3] or [0AF4] or [0AF5] | (Some file): [0B00] or [0B01] or [0B02] or [0B03] or [0B04] or [0B05]
Problem: Apparently you have incomplete cleo library installation
Solution: Download and install it using this link

Last command: (NewOpcodes.cleo): [0D01] or [0D02] or [0D03] or [0D04] or [0D05] or [0D06] or [0D07] or [0D08] or [0D09] or [0D0A] or [ 0D0B] or [0D0C] or [0D0D] or [0D0E] or [0D0F] or [0D11] or [0D12] or [0D13] or [0D15] or [0D16] or [0D17] or [0D18] or [0D19] or [0D1A] or [0D1B] or [0D1C] or [0D1D] or [0D1E] or [0D1F] or [0D20] or [0D21] or [0D22] or [0D23] or [0D24] or [ 0D25] or [0D26] or [0D27] or [0D28] or [0D29] or [0D2A] or [0D2B] or [0D2D] or [0D2E] or [0D2E] or [0D2F] or [0D30] or [0D31] or [0D32] or [0D33] or [0D34] or [0D35] or [0D36] or [0D37] or [0D38] or [0D39] or [0D3A] or [0D3B] or [0D3C] or [0D3D] or [ 0D3E] or [0D3F] or [0D40] or [0D41] or [0D42] or [0D43] or [0D44] or [0D45] or [0D46] or [0D47] or [0D48] or [0D49] or [0D4A] or [0D4B] or [0D4C] or [0D4D] or [0D4E] or [0D4F] or [0D50] or [0D51] or [0D52] or [0D53] or [0D54] or [0D55] or [0D56] or [ 0D57] or [0D58] or [0D59] or [0D5A] or [0D5B] or [0D5C] or [0D5D] or [0D5E] or [0D5F] or [0D60] or [0D61] or [0D62 ] or [0D63] or [0D64] or [0D65] or [0D66] or [0D67] or [0D68] or [0D69] or [0D6A] or [0D6B] or [0D6C] or [0D6D] or [0D6E] or [0D6F] or [0D70] or [0D71] or [0D72] or [0D73]
Problem1: NewOpcodes.cleo not installed, check if this file is inside your CLEO folder.
Solution1: Download and install the latest version of NewOpcodes created by DK22Pac. Click here to download.
Problem2: Even installed it can cause problems, crashes apparently for no reason.
Solution2: Either stop using mods or try to find the problem, who knows how to install/reinstall msvcp100d.dll and msvcr100d.dll? I don't know much about such solutions, let us know if you find more solutions!

Last command: [0B20] or [0B21]
Problem: Apparently you don't have the ClipboardCommands.cleo file in the cleo or Modloader folder
Solution: Download and install it using this link (if you are using Tuning Mod, know that this file already comes in the download, check the mod installation.)

Last command: [038B]
Problem: Loading a model
Solution: Some model that mod cleo uses is missing or buggy in your GTA. Inside scrlog.log, above the last command you will possibly see a "REQUEST_MODEL" with a number in front, the number in front is the model ID (be it car, pedestrian or object). Check the problem, especially installing the mod.

Last command: [0541]
Problem: Apparently Mod Shell problem
Solution: If it was in the Learning To Fly mission, install the fix that comes with the Mod Shell download here at MixMods (currently it already comes with the fix together). If it wasn't in the mission, possibly it was some cleo mod that controls/adds weapons to some vehicle, thus only manually correcting cleo or deleting it.

Last command: [0AA5] [0AA6] [0AA7] [0AA8]
Problem: Some function was called incorrectly by mod.
Solution: It is highly possible that the reason was the arguments passed to the function and you have to hire the author. If you are experienced and the author, see modloader.log for the address, as well as the last (first in the list) addresses in Backtrace, reading the .exe at those addresses to try to understand which of the arguments had the problem. The value of "Access violation reading location" is also very important as it literally shows what value was read, so you can know for example if you passed any null arguments.

Last command: [0AAA]
Problem: Could be caused by some script mod that misused function opcodes like 0AA5:
Solution: If so, you should totally ignore which script crashed in 0AAA, it could be that the error came from a totally different mod.

Last command: [04EE]
Problem: Not found .ifp file.
Solution: Right in front of the command is the filename, and this can help you identify the mod or problem. If it is "SEX.ifp" (that is, it is "REQUEST_ANIMATION SEX") at the time of hot coffee, it is because you are installing GTA SA without hot coffee (version not 1.0). It is recommended that you download the official installation of version 1.0 of GTA SA here. There is a minor download patch here (200MB). If Steam or RGL version, downgrade.

Last command: [00FE]
Problem: Usually crashes here as a CLEO mod didn't check for such a person before checking their location.
Solution: For those who create CLEO mods, it's simple, just check if that person exists before doing anything with them. Whoever installs the mods needs to identify which and notify the author. The Car Dealership mod has had and has been fixed, many mods can have the same problem, it's common.

Last command: [5101]
Problem: Some variable problem.
Solution: If this happened in the Attach Vehicles mod (may be another), update it together with CLEO+. It has been corrected.


By scripts:

script name
Mod: None
About: It was a main.scm error (original GTA script), if you are using normal main.scm (with game missions etc), crashes can happen for example at the gym, it was a Rockstar error (? or incompatibility with another mod ?), or else your save game is not compatible with that main.scm/script.img. Detail that SilentPatch corrects some of these errors. It could also be some rare cases of mods, in which case you won't be able to identify it.

script nebo
Mod: Skybox
About: It usually has a damn crash, bad script, I don't recommend using it, use Real Skybox.

script newsvan
Mod: Steering (Active Dashboard)
About: If you die in the car, it is because you have an old version of Steering. Download the latest version of Steering from MixMods.

script suspens
Mod: Air Suspension v1
About: Usually the mod crashes with the last command: "[81F3]", it was my own mistake from the time I was a noob... to avoid this crash, just always turn off the air suspension when getting out of the car.

script tuning
Mod: Tuning Mod, or possibly another mod named "Tuning"
About: Was it really the Tuning Mod? Please send us the SCRLog here in the comments by putting it on pastebin.com and sending us the link we will try to fix.

script Horn An
Mod: Horn Anim (horn animation)
About: It has already been fixed. Download again.

script mydak
Mod: Don't hit women v2
About: This mod was crashed in the last command [051A] and was actually incompatible with another cleo mod.

script Djjr Ca
Mod: Djjr Car Spawner
About: Trying to spawn train/boat? This will be fixed in Djjr Car Spawner v1.1. For now to fix it just leave "PutOnVehicle = 1".

script intro2
Mod: Actually it was in the script for the second mission of the game where it is usually caused by incompatibilities with CLEO mods.
About: Read "Problem 1" of crash "0x00536BE0" (ctrl+f and look for it up there in the list)

script nanava
Mod: Start / stop the engine. It has already been removed from MixMods, remove it from your GTA, it really is poorly done.

script attach
Mod: It could be several, probably Attach Vehicles. It crashed but has now been fixed.

script ehi ene
Mod: Enterable Hidden Interiors, just download it again it is fixed.

Others

Error: CLEO.asi
P
roblem: Some CLEO/SCM script.
Solution: The SCRLog mod can tell you exactly which script caused the problem and contact the author.

Error: CLEO+.cleo

Problem: Algum script CLEO/SCM que use CLEO+.
Solution: The SCRLog mod can tell you exactly which script caused the problem and contact the author.

Error: modloader.
asi
Problem 1: In extreme cases where you install any file in modloader and it already causes several crashes, including in modloader.asi just by opening the game, probably all your modloader got into a mess and stopped working.
Solution 1: So, try to reinstall modloader and delete all its cache in your user's AppData folder, that is, in my case it would be "C:\Users\JuniorDjjr\AppData\Local\modloader", go in there and delete everything and try again. If you're having trouble finding your AppData folder, please Google it.
About 1: If it crashes after a few minutes of playing: Usually this problem is caused not by Mod Loader, but by ImVehFt. The error is not Mod Loader, but how ImVehFt was created, try to uninstall it or use IVF version 2.0.8 to see if it solves, if it doesn't or you don't use IVF then the problem is really different. ..
About 2: You may also have the wrong Mod Loader, misconfigured etc, review these questions if you configured it.
About 3: Send the modloader.log to see, by the .dll shown at the end of the crash codes you can also get a sense of what kind of file the modloader failed when trying to load. That's if you have the .dll.... So, send it, but there is no promise that it will fix it, modloader crash can be many and many reasons that are difficult to know exactly why...

Error: std.stream
.dll or STDSTR ~ 1.DLL
About: It may be some script that tried to load a non-existent model, for example some script that uses an animal model and creates using cleo, if the animal model is not installed it will crash this dll. This crash can also be easily encountered when using Skin Selector with bad skin installation, such as when installing skins with very long names (warned in Readme to use names with a maximum of 7 letters). Not only skins, anyway, this crash is caused by models in general and not only scripts, it can also be caused by map mods missing .dff .txd and .col etc files, usually the lack of these files in some mod causes the crash on this dll.

Error: V_HUD_by_D
K22Pac.asi
Problem 1: Start the game?
Solution 1: Check the installation, reinstall the mod, check the game's resolution etc, you might even try to remove the GTA San Andreas User Files folder from the Documents.
Problem 2: When selecting the Skin Selector clothing menu?
Solution 2: ...Possibly the mods are really incompatible...

Error: imvehft.as
i
Problem 1: Crash randomly while playing? After playing a few minutes?
Solution 1: Try installing the old version (at the end of this post).
Problem 2: Crash on startup?
Solution 2: Do not install it inside the Mod Loader. Have GTA SA installed in some folder not very long, leave your GTA folder in Documents or any drive you have, very long folder addresses can hit the loading limit of files for this mod.
Problem 3: Crash on Windows 10?
Solution 3: Try to start the GTA in Windows 7 or Windows 98 compatibility mode, in addition to administrator mode. Let me know if it's solved!

Error: std.bank.d
ll
Problem 1: Some sound. This DLL is Mod Loader, but it cannot necessarily be Mod Loader problem.
Solution 1: If you've edited your game's sounds, whatever the mode, back it up, and as always, if it doesn't help, move the GTA folder to Documents and try again.
Problem 2: Possibly your PC's sound problem, DirectPlay.
Solution 2: Read the Error: DSOUND.dll
 (ctrl + f)

Error: D3DXAPI.as
i
Type: Loading failure or crash
Solution 1: Download and install DirectX End-User Web Installer (in this download will come update for all DirectX of your PC, so it can fix other problems as well)
Solution 2: Download and install Visual C ++ 2013 Redistributable
Solution 3: If you have plugin.dll in your GTA, delete it. If you say that plugin.dll is missing, update the mods that need it, as they have been updated and you should no longer use plugin.dll in your GTA.

Error: TM.asi
Typ
e: Loading failure
Solution: Download and install Visual C++ 2013 Redistributable

Error: KERNELBASE
.dll
Type 1: Crash
About: It is a general Windows dll so it can be caused by many different and generic issues like memory allocation. The "backtrace" at the end of the log better tells the source of the problem, contact someone experienced.
Problem 1: Already reported when using peds pack in hd
Solution 1: Identify and remove the buggy pedestrian.
Type 2: Crash when trying to open the game along with "Runtime Error!".
Problem 2: Possibly your PC sound problem, DirectPlay. It could also be a problem with the ModLoader cache. Go to the folder "C:\Users\(USER)\AppData\Local\modloader" where "(USER)" is your username, and delete all content. Next time your game will take a while to open, but it will work.
Solution 2: Read Error: DSOUND.dll
 (ctrl+f)
Type 3: Crash when installing a grams mod with SkyGfx installed
Issue 3: Grass models mismatch.
Solution 3: Disable "ps2grassFiles" from SkyGfx1.ini (and other .ini from it)
Problem 4: CLEO_CALL/SCM_FUNC limit of some CLEO mod.
Solution 4: If so, the SCRLog will say exactly that, and which script it was. If it happens to you, contact the author to fix it, CLEO_CALL is probably being called without returning.
Problem 5: Misconfigured .ini file (wrong letters or characters in an option of an .ini file).
Solution 5: Identify and fix it, it has happened for example when using "FFFFFF" instead of "0xFFFFFF" in MixSets.

Error: bass.dll
T
ype: Any error message related to it, or it is missing from your GTA after uninstalling SAMP.
Solution: Download bass.dll by clicking here, install x86 (32 bits). I recommend downloading even if you don't have the problem, because some mods that use sounds or the SAMP .dll may have problems etc.

Error: quartz.dll

Problem 1: Incompatibility with new versions of Windows.
Solution 1: Enable Windows XP Compatibility Mode (Service Pack 2) in the game's .exe properties.
Problem 2: Related to Pluguin LAV Video
Solution 2: (uploaded by Guto Rocha) In Start Menu > Programs > K-Lite Codec Pack > Configuration. Click on LAV Video. In the "Formats" tab, clear the boxes corresponding to MPEG1, MPEG2 and MPEG3 formats. Apply and ok. (tested on Windows XP and Windows 10).
Problem 3: It has been reported when installing mods in the Mod Loader root folder instead of installing in folders inside it, which is an error.
Solution 3: Do not install mod files by leaving in "GTA San Andreas / modloader /", always install the files in "GTA San Andreas / modloader / some folder". There is more information right in the Modloader download post.

Error: colormod.a
si
Problem: It has already been reported as incompatibility with Project2DFX. Even if it doesn't make much sense and even I used them both together a lot and I never saw a problem, but you can try to uninstall either one to see if it corrects. Crash was reported as soon as the game started with the two together. As well as it can also be incompatibility with some other mod, or even bad installation of Color Mod.

Error: igdumd32.d
ll
Problem: This .dll is from Intel Graphics (your video card). It could be a problem with your PC's graphics drivers, or simply a conflict between graphics mods, or a problem model or texture mod. It's hard to know the exact reason since it's about graphics in general.

Error: DSOUND.dll

Problem: DirectPlay
Solution 1: Use SilentPatch
Solution 2: (uploaded by Luiz Felipe): Install DirectPlay by going to Control Panel>Programs and Features>Turn Windows features on or off (on the left of the window)>go to legacy components and check the DirectPlay box>install and restart the computer (tested on Windows 8.1 and fixed).

Error: normalmap.
asi or NORMAL~1.ASI
Problem 1: Video card not supported? If your video card is very old, this is possibly the problem.
Problem 2: Wrong Installation? Avoid Mod Loader to install Ryosuke mods like this one.

Error: colormod.a
si
Problem: Incompatibility with Project2DFX
Solution: Uninstall it or it or Project2DFX.

Error: msvcr100.d
ll msvcp100.dll msvcr110.dll msvcp110.dll msvcr120.dll msvcp120.dll msvcr100d.dll msvcp100d.dll msvcr110d.dll msvcp110d.dll msvcp120d.dll msvcp120d.dll msvcp120d.dll d3d_d3.dll_d3_26.dll
Type: Asked for the DLL or some problem with it.
Solution: Click here to go to the post with the download of all of them.

Error: STREAM~1.A
SI
About: Check ImprovedMove post: https://www.mixmods.com.br/2019/10/Improved-Move.html

Error: STREAM~1.A
SI
About: Stream Memory Fix? If you use this your GTA is out of date. As I always say, avoid mounting your GTA on other sites outside of MixMods, the Stream Memory Fix is something from 2007, nowadays it is replaceable by other things much better like MixSets and Open Limit Adjuster. Click here for the post on how to put together a good GTA.

Error: d3d9.dll
P
roblem 1: As you may already know, it's the .dll used for a lot of things, especially enb series, so everything sets it to WHAT you used it (where 99% of people use it as enb series or it already came in game installation ). It may be that your PC doesn't support enb series or another graphical mod that uses this dll, but there are also mods that are made using this dll, super old mods from the GTA SA release where they ended up using this .dll to create the mod , completely obsolete now, stop using such mods. If you don't use enb series or other mods of this dll, it should be correctable by updating your DirectX Runtime, and then, if you have this dll installed in your game, delete it (or not).
Problem 2: If it crashed on a mission, strangely this dll can crash and the solution sent by Luiz Felipe says that you simply have to skip the cutscene by pressing Enter. It can be caused by some buggy caption or other text on the screen, usually by translations or mods, in this case, it is better to contact the creator and / or disable the captions or skip the cutscene if possible. Gamevicio's translation has this crash, our translation pt-br doesn't.
Problem 3: If a crash in the Advanced menu of the game graphics and you are using 90s AVP Reborn, it was caused by his Super GT and the solution is simply to change this car. In the same way you might not be using the 90s AVP but you might have this same car, or another car with the same problem, that is, if this dll crashes in this menu, it could be a car installed in your GTA.
Problem 4: During an explosion? Using some mod like Remastered Effects? If you have any 0x007FDE14 and/or 0x007FE7DC and/or 0x004A140A in the "Backtrace" at the end of the log, it may be caused by IgnoreWater from MixSets (or even FreezeHour). So, if enabled, set these functions to -1 in MixSets.

Error: ntdll.dll

Problem: Difficult to know the exact reason as it is a very common Windows .dll. But it's more likely something to do with uploading files.
First of all, if the crash occurred when opening the game, simply try to open it one or two more times that should work. It's weird and I still don't know why yet. But this same error can be caused by other things:
Solution 1: At the end of "modloader.log", in the top line of the crash address, you will have the last file read, for example: "Loading default object types "data\maps\veh_mods\veh_mods.ide"", in this example , possibly crashed when trying to read the veh_mods.ide file, check it. If the last file was a .txd, it was quite possibly not a problem with it. Also often it can't have anything to do, as for example, if you enter a store it will appear that "shopping.dat" was loaded last, but that doesn't mean that the crash was in this file too, so be wary not sure, but still try to check them, especially if the crash was when trying to open the game.
Solution 2: Check Windows permissions and file reads, it can be any file, whether from the data folder or from some mod. I always recommend using GTA in Documents and not Program Files, fix this and other problems.
Solution 3: If it crashed when selecting the radio "User Tracks", delete the file "sa-utrax.dat" from the folder "Documents/GTA San Andreas User Files". It is also possible that some .mp3 there is with the wrong encoding, GTA SA only accepts the MP3 LAME format. This could also be a current CLEO mod issue, explained here: https://github.com/cleolibrary/CLEO4/issues/38 in this case you can identify and remove such a CLEO mod that uses the CHDIR command, or change the radio by pause menu.
Solution 4: If SAMP crashed, check if "SAMP Fix" is marked in the ImVehFt .ini. Or if any files needed for SAMP to work are missing (in this case reinstalling SAMP will help)
Solution 5: If you see followed by an error window "std.asi: translator.SteupASI failed to identify caller ASI", it is because it was incompatibility of one .asi with another, mods .asi that modify the same thing as the other. I believe this was once due to vehlightsfix.asi along with silentpatch.asi, as they both fix some of the same things, but that was just a guess and also just an example.
Problem 6: Action_x86.dll incompatible with ntdll.dll.
Solution 6: Switch to 32-bit color resolution.
Problem 7: When entering an interior? According to Luiz Felipe, possibly you use the mod HiDefCam.asi, took a photo with the streaming memory (stream memory) at the limit and then entered an interior where it caused the crash.
Solution 7: Uninstall HiDefCam.asi.
Problem 8: After minimizing the game?
Solution 8: Pause the game before minimizing, or if you have already paused it, it could be the mod SAGrading (colorcycle).
Solution 9: Try installing Improved Fastloader.
Solution 10: The stream.ini file is missing from the game folder.
Solution 11: Don't use special characters (no punctuation etc) in the game folder name or somewhere along the path. Also don't go too long. Has already been fixed after removing characters [ and . of the game folder name, but it is not exactly known if this was the problem, or if the path was too long, or if it was some Windows bug etc.


Other problems:

Error: Freeze (us
ually flying with Hydra)
Solution: Open the game in administrator mode and Windows XP SP2 compatibility mode. It could be some mod, you don't know which one.

Error: Game not r
einstalling
About: Trying to use the installer but it already identifies that the game is installed?
Solution: Open the start menu, type regedit and open regedit.exe. Go to HKEY_LOCAL_MACHINE -> SOFTWARE, there will be a "folder" Rockstar Games, and inside GTA San Andreas with a "key" inside it. Delete the key or the "GTA San Andreas" folder itself.
If not, look inside HKEY_CURRENT_USER.

Error: Message "R
untime Error!" "This application has requested the Runtime to terminate it in
an unusual way."
About: It could be caused by an error in some .asi mod. The "modloader.log" or other crash dump can give a hint of what the mod was (even if not 100% correct).
During gameplay: In addition to .asi, it may have been caused by high memory usage if you configured the game to use 2GB of stream memory without using largeaddress.
When trying to start the game: In addition to .asi, it may be ModLoader's cache problem. Go to the folder "C:\Users\JuniorDjjr\AppData\Local\modloader" where "JuniorDjjr" is your username, and delete all content. Next time your game will take a while to open, but it will work.
