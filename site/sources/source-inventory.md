# Source inventory

| Category | File or URL | Version/date | Authority | Imported | Notes |
|---|---|---|---|---|---|
| Mainline structured baseline | https://github.com/PokeAPI/api-data | Pinned in `baseline.lock.json` | Generic fallback | Generated | Never overrides current hack documentation. |
| Mainline sprite baseline | https://github.com/PokeAPI/sprites | Pinned in `baseline.lock.json` | Generic fallback | Generated | Replace missing/custom form assets deliberately. |
| Official documentation bundle | `sources/inbox/official-v1.4.1/` | v1.4.1; changelog dated 2023-06-24 | AphexCubed/Drayano primary documentation | Yes | Nineteen text files; authoritative for Pokémon, moves, evolutions, encounters, trainers, gifts, trades, items, legendaries, modes and special rules. |
| Community wiki and structured datasets | https://smilingzero.github.io/BlazeBlack2ReduxWiki/ (`sources/inbox/community-wiki/`) | Git revision `bbbc76b84806629bce625579dd182d7baea63e9e`, 2024-12-24 | SmilingZero community reference | Yes | Generated from Redux documentation; provides structured Pokémon, encounter and trainer tables. Official v1.4.1 files take precedence. |
| Pokédex, forms and stats | `official-v1.4.1/Pokemon Changes.txt`; wiki `scrapedJSON/pokemon/` | v1.4.1 | Primary plus structured community transcription | Yes | 649 species and 673 documented forms imported for the Complete ruleset. Unsupported later-generation baseline forms explicitly removed. |
| Abilities | Same as Pokédex source; wiki API cache for descriptions | v1.4.1 | Primary plus generic descriptions | Yes | All documented ability slots imported. Descriptions remain PokeAPI-derived explanatory text. |
| Evolutions | `official-v1.4.1/Evolution Changes.txt`; wiki Pokémon JSON | v1.4.1 | Primary plus structured community transcription | Yes | Single-player evolution methods and Redux item evolutions imported. |
| Moves and learnsets | `official-v1.4.1/Move Changes.txt`, `Pokemon Changes.txt`; wiki move JSON | v1.4.1 | Primary plus structured community transcription | Yes | Level, TM and tutor learnsets imported; 84 later/custom moves added beyond the pinned Sword/Shield fallback. Egg learnsets are not claimed as fully verified. |
| Move tutors and services | `official-v1.4.1/Important NPCs.txt`; wiki `data/tutorList.csv` | v1.4.1 | Primary plus structured community transcription | Yes | Compatibility imported. Documentation says locations are unchanged from Black 2; location labels reflect that baseline. Shard costs remain a review item. |
| Wild encounters | `official-v1.4.1/Wild Area Changes.txt`; wiki nested encounter JSON | v1.4.1; wiki fixes through 2024-12-24 | Primary plus maintained community transcription | Yes | 61 locations; seasons, floors, rooms, methods, Hidden Grottos and version-specific encounters preserved as subareas/methods. Source has no day/night split, so entries are marked all-day. |
| Other acquisition methods | Gift, Trade and Legendary official files; matching wiki pages | v1.4.1 | Primary | Yes | Gifts, Gift Eggs, trades, special encounters and legendary quest summaries imported. |
| Items and shops | `official-v1.4.1/Item Changes.txt`; wiki `docs/item.md` | v1.4.1 | Primary plus structured community transcription | Yes | 276 changed item locations/costs imported. Unchanged item definitions and descriptions remain baseline-derived. |
| Trainer battles | `official-v1.4.1/Trainer Changes.txt` | v1.4.1 | Primary | Yes | 457 teams imported with mode, location, condition, ability, level, item and moves where documented. |
| Trainer profile, starter and rival rules | Gift and Trainer documentation | v1.4.1 | Primary | Yes | Snivy/Tepig/Oshawott and Hugh counter-starter mapping configured. Nate/Rosa plus legacy Hilbert/Hilda sprites come from the supplied wiki repository. |
| Badges | Black 2 progression, names verified against trainer documentation | v1.4.1 | Primary/baseline | Yes | Eight Unova badges configured; generic local badge marker art is used. |
| Branding artwork and colour palette | https://www.steamgriddb.com/game/5313303 | Selected 2026-08-17 | SteamGridDB contributors Anon11926, Kam and 8resolution | Yes | Local hero, logo and icon assets are credited in `assets/art/STEAMGRIDDB_CREDITS.md`; the cyan/steel/gold interface palette was derived from them. |
| Maps | None supplied | — | — | No | Map feature disabled; no unlicensed map was inferred. |
| Sprites and artwork | Pinned PokeAPI sprites; wiki trainer sprites; SteamGridDB branding | Pinned commits/current wiki revision; selected 2026-08-17 | Generic fallback/community/contributor artwork | Yes | Local normal and shiny Pokémon sprites are pinned. SteamGridDB hero, logo and icon are stored locally with direct attribution links. |

## Conflicts, gaps and confidence

- The official files call the variants Complete/Classic and Complete EVless/Classic EVless. The field guide displays the Complete data by default because the detailed Pokémon tables describe that ruleset; mode-specific trainer conditions remain labeled.
- Redux mixes Gen V engine behaviour, Gen VIII stats/abilities/TM assumptions, later-generation selected moves, Fairy typing and Gen VI Steel resistances. `sword-shield` is therefore the nearest generic baseline, not a claim of exact mechanics parity.
- The community wiki fixes some encounter transcription after the v1.4.1 text bundle. It is used for structure and later table corrections; the official text remains authoritative for meaning.
- Battle natures and EVs are not included because the official documentation states that trainers use random natures and no EVs in this Gen V implementation.
- Cloud sync and region maps remain disabled; user-supplied SteamGridDB branding is enabled and deployed.
