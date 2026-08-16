# SCFIX-Liberty

SCFIX-Liberty aims to provide bugfixes to the original scripts. Based off of [UndefinifiedLiberty](https://github.com/Sergeanur/UndefinifiedLiberty).

All changes to the scripts were marked with `SCFIX` comment.

Currently in beta status.

"BW" in the list of changes refers to changes made to accommodate Fire_Head's [Breakable Windshields](https://github.com/Fire-Head/IIIBreakableWindshields) mod.

## Download SCM

Get latest release here: https://github.com/Sergeanur/SCFIX-Liberty/releases

## Installation

Replace main.scm inside data directory, but read save files compatibility note below first.

## List of changes

- Removed inability to start a mission if you jump onto a marker
- Fixed an extra reward not being given to the player in a mission "Smack Down"
- Fixed bums inside Portland tunnel spawning endlessly by standing on a tall vehicle
- Fixed destination blip position in a mission "I Scream, You Scream"
- Fixed Claude being seen as a boat driver during the cutscene in a mission "Last Requests"
- Fixed Securicar scratching the wall when driving into the garage in a mission "Escort Service"
- Fixed multiple issues in "Decoy": SWAT chasing the player if they get wanted level on the way to the van, and Army chasing the player if they use Pay 'n Spray during the chase
- Fixed starting marker for the mission "The Fuzz Ball" changing its position after beating "Chaperone" mission
- Fixed Portland Harbor population disappearing after missions "Cutting the Grass" and "Bomb Da Base: Act II"
- Restored cut subtitles in "Bomb Da Base: Act I" cutscene
- Made "Bomb Da Base: Act II" count mission attempts correctly when re-attempting the mission
- Disabled Unique Stunt Jumps camera activating when driving Dodo
- Mafia shotguns are now being replaced with Uzis when activating Paramedic, Vigilante, Firefighter or Taxi Driver side activities (similarly to missions "Big'n'Veiny" and "Espresso-2-Go!")
- Fixed starting position for "Multistorey Mayhem" - now it triggers as soon as you enter the parked Stallion
- Fixed mission triggers for "Gripped!" and the RC missions starting when the player parked the car on the trigger
- Fixed blip for Diablo missions staying after beating "Last Requests"
- Fixed taxi driver being able to become your passenger in a Taxi Driver side activity
- Fixed multiple markers showing at the hospital in Paramedic
- Restricted peds from spawning at covered areas of Staunton in Paramedic
- Changed patients behavior to only run towards stopped ambulance instead of while it's still moving in Paramedic
- Fixed dropped off patients in Paramedic walking away instead of running to the hospital
- Finishing 12 levels of Paramedic now prints "Ambulance missions complete!" instead of "Paramedic mission ended." as originally designed
- Bridge model swap by the intro cutscene made seamless
- LCPD wall model swap in "Kanbu Bust-out" made seamless
- Panlantic fence model swap in "Grand Theft Aero" made seamless
- Fixed Quadruple Insane Stunt
- Reimplement "Bling-Bling Scramble" random selection of a checkpoint pattern to fix the third pattern being unreachable
- Reimplement "Plaster Blaster" random selection of an ambulance path to fix the third path being unreachable
- Implemented fixes for potential SSU in the intro cutscene script
- Removed duplicate models loads during the jailbreak cutscene
- Fixed some models not being marked as no longer needed after being loaded by the jailbreak cutscene
- Fixed On Mission flag (flag_player_on_mission) sets to prevent any abuse of this flag
- Removed On Mission flag checks in some mission that were meant to bypass compiler errors
- Re-enabled a Bobcat spawn in front of the Supa Save in Portland that was never switched on due to its script handle getting reused
- Fixed the wanted level tutorial briefly pausing the game to load the models
- Fixed "Arms Shortage" attempting to unload the incorrect models
- Fixed the car blip in "Pump-Action Pimp" not disappearing if one of the characters was killed inside the car (for BW)
- Removed unsafe code in "Cipriani's Chauffeur" operating on a stale handle to Toni's car
- Added extra death checks for Toni in the first half of "Cipriani's Chauffeur" and interrupted Toni's "no fancy crap" line if he's hurt (for BW)
- Fixed a 1-frame window where the player could leave the car in the initial cutscene in "Cipriani's Chauffeur" and added a timeout to that cutscene to avoid softlocks
- Added driver health checks in "Dead Skunk in the Trunk", so Forellis start chasing the player if one of the cars is destroyed instantly or if the driver is hurt (for BW)
- Added a sound when collecting checkpoints in "Turismo" to match the other checkpoint missions
- Made "Paparazzi Purge" pass when the reporter dies instead of when the boat explodes (for BW)
- Skipping the initial cutscene with thw two Yardies in "Uzi Rider" now clears the subtitles and audio
- Fixed "Uzi Rider" modifying the population density in Hepburn Heights permanently
- Added a check for the Shoreside Vale Pay 'n Spray in "Uzi Rider", as per the original TODO comment in the source
- Fixed "Uzi Rider" softlocking if the car gets destroyed instantly
- Made "Uzi Rider" fail if the player attacks one of the Yardies in the car (for BW)
- Fixed the final subtitle lingering on-screen when skipping the phone cutscenes in "Bling-Bling Scramble", "Uzi Rider", "Gangcar Round-Up", and "Kingdom Come"
- Made "Bait" fail if any of the vehicle occupants dies, instead of checking for their cars (for BW)

## Save files compatibility

At this point it's incompatible with old save files made with original scm. In future it's possible to come up with a save file converter once a stable release will be decided upon.

## How to compile

You need to get miss2.exe from 3master and then patch the 3master plague out of it.
To patch miss2.exe, put it in `patch` directory and launch **xdelta3.bat**. Now you can use miss2.exe that would produce correct compiled binaries.

