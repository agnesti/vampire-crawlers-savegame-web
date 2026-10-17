[Versión en español](README(Spanish).md)

A web page to view and edit the save file (`SaveProfile0.save`) of **Vampire Crawlers**. It runs in your browser, needs no installation, and **your file is never uploaded anywhere**: everything happens on your own device.

**Use it now:** https://agnesti.github.io/vampire-crawlers-savegame-web/

## What it does

- **Summary** of the save: coins, party, characters, play time, state and progress.
- **Coins:** stored in two places in the file (`ProfileSaveData` and `ProgressionSaveData`); the game uses the progression one, so the page updates both at once.
- **Characters:** list of the 21 known ones; tap one to mark it as purchased or remove it.
- **Dungeons:** which ones you visited, which one is selected and, *experimentally*, each one's `Unlock_*` achievement.
- Game modes, tutorials, relics and permanent upgrades (enabled and level).
- **Full JSON** view with search (matches are highlighted and scrolled into view) and shortcuts to each section, for manual edits.
- **Compare:** load two saves and see what changed between them (achievements, characters, cards, gems, metrics…).
- **Restablecer** (reset): goes back to the values of the file you uploaded if you touch something by mistake.
- A warning when the save was taken **mid-run**.
- **Hacer checksum** (make checksum): computes the real checksum and downloads the file in the same format the game uses. It enables as soon as you change anything.
- Downloads a **backup copy** of the original before you replace it.

Number fields only accept digits and show the numeric keyboard on phones. The interface is currently in Spanish.

## How to use it

1. Back up your save file.
2. Open the page, click **Seleccionar archivo** (select file) and choose `SaveProfile0.save`.
3. Change what you want in **Resumen** (summary) or **JSON completo** (full JSON).
4. Click **Hacer checksum**. The file is downloaded with the same name.
5. Copy it into the save folder, replacing the original.

## About the checksum

The `Checksum` field is the SHA-1, base64-encoded, of the `Data` block written with 2-space indentation and Windows line endings. When a file is loaded, the page checks whether its checksum matches that calculation (shown next to the file name). If it does not match, the field is left empty on export, which the game also accepts. The page keeps the file's original formatting (line endings and numbers such as `24.0`) so the result is identical to what the game writes.

## Where the save file is

- **Windows (Steam):** `%USERPROFILE%\AppData\LocalLow\Nosebleed Interactive\Vampire Crawlers\Save\SaveProfile0.save`
- **macOS:** `/Users/<username>/Library/Application Support/com.poncle.vampirecrawlers/Save/SaveProfile0.save`

More paths on [PCGamingWiki](https://www.pcgamingwiki.com/wiki/Vampire_Crawlers:_The_Turbo_Wildcard_from_Vampire_Survivors#Save_game_data_location).

## Warnings

- Use this tool at your own risk and always keep a copy of the original.
- Edit saves taken from the main menu. With a run in progress the game may overwrite your changes.
- If Steam warns about a cloud sync conflict, keep the local (newer) file.
- Do not set coins to the maximum value (2147483647): it is the limit of a 32-bit integer and may overflow. Something like 999999 leaves headroom.
- Upgrade levels above the normal maximum are accepted by the game, but their effect is capped in a run. For example, *Might* shows a higher value in the main menu, yet damage stopped at 1000% in dungeons (reached at level 49 in the author's test).
- Buying characters or unlocking dungeons by hand is not verified in every case. Try it on a copy first.
- Tested with saves from versions `0.22.0` and `0.30.0`. If an update changes the format, parts of the tool may stop working.

## Credits

- Based on the idea and finding of [Kartones' editor](https://github.com/Kartones/vampire-crawlers-savegame-editor), which in turn cites [this article](https://www.neonlightsmedia.com/blog/vampire-crawlers-save-transfer-game-pass-steam): the `Checksum` field can be left empty.
- Character and coin icons: [Vampire Survivors Wiki](https://vampire.survivors.wiki/w/Crawlers:Wiki), licensed under [CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/). They are loaded from the wiki; offline, a letter is shown instead.
- Fan project, **not affiliated with poncle or Nosebleed Interactive**. Vampire Crawlers and Vampire Survivors belong to their respective owners.
