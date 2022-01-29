# Open Star Ruler
Developed by Blind Mind Studios from 2011-2017 and first launched in March 2015,
Star Ruler 2 is a massive-scale 4X/RTS set in space. Explore dozens, hundreds,
or even thousands of systems in a galaxy (or galaxies) of your choosing, expand across their
planets, exploit the resources you find, and ultimately exterminate any who
stand in your way. The fate of your empire depends on your ability to master
the economy, field a military, influence galactic politics, and learn what you
can about the universe.

Open Star Ruler is a community-led attempt to maintain and upgrade the original game
with as little impact as possible upon its compatibility with the commercially distributed
binaries from Steam and GOG.

## What is this?
This repository contains all the secondary scripts, data files and assets required to run OpenSR.
It is used primarily as an immutable source of truth for OpenSR installation, virtually identical to
the commercial assets, but there have been rare instances where the original data files
needed to be changed outside the scope of the OpenSR Modpack.

## Playing the Game
The Star Ruler 2.exe contained in the main folder is just a launcher. To run
the game you will need to build the binaries for your platform from source, or install
the game via the OpenSR Launchpad.

## Differences with Commercial Version
* The game's soundtrack was never open-sourced, and the OpenSR team has not chosen any replacements.
  The OpenSR Launchpad can install OpenSR as an upgrade on top of an existing commercial installation.
  The commercial version's music will then automatically be detected and played.
* All code for accessing the SteamWorks API has been removed. The game platform abstraction layer `game_platform.h` has 
  been kept intact, so other mod-sharing platforms could potentially be integrated into the game.
* Code for the automatic game patcher that is part of the GOG.com release is part of the repository, but the functionality
  is disabled, since it relies on delta updates and does not work with OpenSR at this time.
* While the actual source code is probably still compatible with 32-bit platforms, project files and external dependencies for
  32-bit builds were not included in the source dump, nor have they been replicated by the OpenSR team at this time.

## FAQ
### Can I Play Multiplayer with Steam/GOG versions?
In theory (see #1). The original open-source dump by Blind Mind was stated to be multiplayer-compatible with the commercial versions.
However, in practice, there have occasionally been anomalies and unexplained crashes that may not have been fully resolved yet.

If you absolutely must make multiplayer-incompatible changes to the open source version, 
please remember to change the `MP_VERSION` identifier in the `scripts/definitions/version.as` file
in the OpenStarRuler-Data repository, so things do not break from people with incompatible versions trying to join each other.
Be advised that multiplayer-incompatible changes to the Starflare engine are to be avoided whenever possible until further notice,
and that unless it is absolutely necessary, multiplayer-incompatible changes to the game data should be submitted to the OpenSR Modpack,
*not* OpenSR-Data. Pull requests not adhering to these criteria will be held under severe scrutiny and probably rejected.

### Does this have the Wake of the Heralds DLC Expansion?
Yes. Blind Mind modified the code to bypass all DLC checks and unlock it by default. The Wake of the Heralds content
is always available in OpenSR.

### Is there a Community?
Most Star Ruler 2 community activity is centered around the [Steam Forums](https://steamcommunity.com/app/282590/discussions/)
(it is possible to post without owning the game on Steam, though Steam activity has dropped off considerably), and the [OpenSR Discord](https://discord.gg/sUJKJDc).

## Licensing
Star Ruler 2 and OpenSR source code are licensed as MIT, art assets are licensed as CC-BY-NC 2.0.

See the COPYING file for more information.
