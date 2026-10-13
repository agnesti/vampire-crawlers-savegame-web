# Savegame editor for Vampire Crawlers

[Versión en español](README(Spanish).md)

A web page to view and edit the save file (`SaveProfile0.save`) of **Vampire Crawlers**. It runs in your browser, needs no installation, and **your file is never uploaded anywhere**: everything happens on your own device.

**Use it now:** https://agnesti.github.io/vampire-crawlers-savegame-web/

## What it does

- Shows a summary of the save: coins, party, purchased characters, play time and progress.
- Changes your **coins**. They are stored in two places in the file (`ProfileSaveData` and `ProgressionSaveData`) and the game uses the progression one, so the page updates both at once.
- Toggles game modes, tutorials, relics and permanent upgrades, and changes upgrade levels.
- Lets you view and edit the **full JSON**, with search and shortcuts to each section.
- **Hacer checksum** (make checksum): empties the `Checksum` field (the game accepts it that way) and downloads the file ready to use.
- Downloads a **backup copy** of the original before you replace it.

## How to use it

1. Back up your save file.
2. Open the page, click **Seleccionar archivo** (select file) and choose `SaveProfile0.save`.
3. Change what you want in the **Resumen** (summary) tab or in **JSON completo** (full JSON).
4. Click **Hacer checksum**. The file is downloaded with the same name.
5. Copy it into the save folder, replacing the original.

The interface is currently in Spanish.

## Where the save file is

- **Windows (Steam):** `%USERPROFILE%\AppData\LocalLow\Nosebleed Interactive\Vampire Crawlers\Save\SaveProfile0.save`
- **macOS:** `/Users/<username>/Library/Application Support/com.poncle.vampirecrawlers/Save/SaveProfile0.save`
- **Android:** /storage/emulated/0/Android/data/com.poncle.vampirecrawlers/files/Save/SaveProfile0.save

More paths on [PCGamingWiki](https://www.pcgamingwiki.com/wiki/Vampire_Crawlers:_The_Turbo_Wildcard_from_Vampire_Survivors#Save_game_data_location).

## Warnings

- Use this tool at your own risk and always keep a copy of the original.
- If Steam warns about a cloud sync conflict, keep the local (newer) file.
- Do not set coins to the maximum value (2147483647): it is the limit of a 32-bit integer and may overflow when you earn more. Something like 999999 leaves headroom.
- Tested with saves using save system version `0.30.0`. If a game update changes the format, parts of the tool may stop working.

## Credits

- Based on the idea and finding of [Kartones' editor](https://github.com/Kartones/vampire-crawlers-savegame-editor), which in turn cites [this article](https://www.neonlightsmedia.com/blog/vampire-crawlers-save-transfer-game-pass-steam): the `Checksum` field can be left empty.
- Character and coin icons: [Vampire Survivors Wiki](https://vampire.survivors.wiki/w/Crawlers:Wiki), licensed under [CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/). They are loaded from the wiki; offline, a letter is shown instead.
- Fan project, **not affiliated with poncle or Nosebleed Interactive**. Vampire Crawlers and Vampire Survivors belong to their respective owners.
