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

The mod itself is one click. It is bundled inside the tool, so you never download mod files separately and you never copy anything by hand. The only thing you set up yourself is SFSE.

1. Install **SFSE**: drop its files into your Starfield folder, next to the game exe.
2. Start **PULSAR** (Pulsar.exe). If you do not have it yet, grab it from the [Releases](https://github.com/ramisotti13-eng/pulsar-tool/releases) on this page, unzip it anywhere except the Starfield folder, and run it.
3. Open the **Setup** page and click **Install mod**. That one click copies the whole mod into Starfield. Then click **Fix all** so the required game settings are set.

New versions install the same way, with one click, from the **Updates** page or the banner at the top of the tool. Close Starfield before installing or updating.

## Play together

Both players run the game through the tool, and **both have to be in game with a save loaded** (not sitting in the main menu) for the connection to work.

1. On the **Co-op** page, type your name.
2. One of you clicks **Host** and shares the code that appears. The other clicks **Join** and enters that code. Starfield launches for both of you.
3. Each of you loads a savegame (see the disclaimer for which one to use). You both need to be loaded in and actually playing, not in a menu, or the link will not come up.
4. Once the connection is made, the host's current game is sent over to the joiner and loaded, so you both end up in the same place in the same world.

**The save sync in step 4 can take a while, so please be patient.** A Starfield save is several megabytes. It has to transfer to the joiner and then load, and during that time it can look like nothing is happening for a few seconds. That is expected. It is not frozen and it is not a crash, just let it finish.

Even though the joiner loads the host's game, your own character is restored right after, so both of you keep your own level, skills, perks and inventory.

Tip: press **F8** in game to regroup at the host after a fast travel, or any time you drift apart.

For a private game without the lobby, use **Play directly**: the host shares an IP and port, and the other joins by IP (over the internet you also forward that port on your router).

## Good to know

A few things that look like problems but usually are not:

* **A character vanishing on a planet is normally not a disconnect.** It is a cell transition: the engine has to reload that character on the other side. Give it a few seconds, or move closer, and it comes back.
* **Lost each other or out of sync? Press F8.** That pulls the client back to the host. It is the manual regroup and it fixes most "where did they go" moments.
* **On a planet surface each of you can fast travel on your own.** The host fast traveling does not drag the client along on purpose. Use F8 afterwards to regroup at the host.
* **The other player is shown as a copy of their character.** A short flicker of that copy when changing cells is cosmetic and known. It does not mean something broke.
* **The first time someone enters a vehicle, the game shows a short tutorial popup.** That popup is local to whoever entered, so the other player will not see it. That is normal.
* **Both of you should load the same fresh savegame** before hosting or joining (see the disclaimer).
* **Close Starfield before you install or update the mod** from the tool.
* **If the tool shows offline, use Reconnect** on the Co-op page. A relay can hiccup for a moment.

## Other mods

I have not tested PULSAR together with other mods yet. Real compatibility testing is a beta thing. It is technically possible to run other mods at the same time, so you are welcome to try your setup and see what works for you. Just expect that during the alpha some combinations may not work or may cause problems. If something breaks, please try again with only PULSAR active before you report it, so we know whether it is PULSAR or a mod clash.

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

## Host your own relay (optional, advanced)

You do not need this to play. A relay just passes traffic between two players when a direct connection is hard, and the tool already picks a working one for you automatically.

You might want your own if you want a private relay for your group, or to contribute one to the public list. The relay is open source, and the full setup (Docker or .NET, plus every setting) is here:

https://github.com/ramisotti13-eng/pulsar-relay

A relay only forwards traffic. It never loads your save or touches your character, and because the connection is encrypted it only ever sees encrypted bytes.

Made by ramisotti13. Thanks for testing the alpha and helping get it stable.
