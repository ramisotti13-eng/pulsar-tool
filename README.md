# PULSAR

Co-op multiplayer for Starfield. Play through the game together with a friend.

> **Disclaimer: this is an alpha.** Please report crashes and bugs that genuinely break your game progress or stop it completely. The alpha exists to get the mod stable.
>
> You can create a report straight from the tool and then upload it on GitHub. For crashes, please add a savegame too if you can.
>
> Most visual bugs are already known and will be handled in the beta.
>
> You can load any savegame. Your character is always the one from that savegame. I do recommend using a fresh savegame, right from the point where you finished creating your character. Load that savegame, and use the same one when you join a lobby.
>
> If you ever need to, you can reset your character any time in the PULSAR tool under Settings.

## What you need

* **Starfield, the Steam version.** The mod loads through SFSE, which only supports Steam. The Game Pass and Microsoft Store version is not supported, and the mod will never run on consoles.
* **SFSE (Starfield Script Extender)**: https://sfse.silverlock.org/
* Windows. A friend with the same setup.

## Install

1. Install **SFSE** from the link above (drop its files into your Starfield folder, next to the game exe).
2. Download the latest **PULSAR** release from the [Releases page](https://github.com/ramisotti13-eng/pulsar-tool/releases).
3. Extract the zip anywhere you like, but **not** inside the Starfield folder.
4. Run **Pulsar.exe**.
5. Open the **Setup** page and click **Install mod**. That copies the mod into Starfield. Then click **Fix all** so the required game settings are set.

That is it for the install. The tool launches the game through SFSE for you.

## Play together

1. On the **Co-op** page, type your name.
2. One of you clicks **Host** and shares the code. The other clicks **Join** and enters that code.
3. Starfield launches for both of you and you are in the same game.

Tip: both players should load the same kind of fresh savegame (see the disclaimer). Press **F8** in game to regroup at the host after a fast travel.

For a private game without the lobby, use **Play directly**: the host shares an IP and port, the other joins by IP (over the internet you also forward that port on your router).

## Reporting a bug

1. In the tool, open the **Bug report** page and create a report. It collects the logs and basic diagnostics into a file.
2. Upload that file to the [issue tracker](https://github.com/ramisotti13-eng/pulsar-tool/issues).
3. For a crash, attach a savegame from right before it happened if you can. It helps a lot.

## What is in the Alpha

* **2 player co-op.** 3 to 4 players is experimental, feedback welcome.
* **Host and join by a short code**, or connect directly by IP for LAN and direct play.
* **Your character carries over.** Level, skills, perks, inventory and credits are saved and follow you between sessions and across savegames. Both of you keep your own progress.
* **Shared combat.** Enemies, damage and kills are synced, and both players get the kill XP in a shared fight.
* **Downed and revive.** When you go down you can be picked back up instead of dying.
* **The world stays in sync.** NPC positions, doors, grabbed objects, time and weather, and basic quest progress.
* **Follow into space and on the ground.** The client comes along through takeoff, landing and ground vehicle driving. Some of this is still rough and gets polished in the beta.
* **Fast travel and regroup.** Travel on your own, then press F8 to pull yourself to the host.
* **Encrypted connection.** All co-op traffic is encrypted, and relays mean you usually do not need to forward a port.
* **Character backup.** Export and import your character to a file, and reset it from Settings whenever you want.

Made by ramisotti13. Thanks for testing the alpha and helping get it stable.
