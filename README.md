# WoW Forever launch data

This repository holds the XP needed per level in World of Warcraft: Forever, its launch time by time zone, the answer to whether it is a private server, and the addon status at launch, prepared with AI assistance by the Realm First desk. Every row names its source.

## How much XP each level needs in WoW Forever

WoW Forever needs 4,084,700 XP from level 1 to level 60. Level 1 to 2 takes 400 XP, level 30 to 31 takes 47,400 and level 59 to 60 takes 209,800. The values are the base-content rows (ContentSetID 0) of the client's `LevelExperience` table, read through [wago.tools](https://wago.tools/db2/LevelExperience?build=1.60.1.70959) on 20 November 2026 for Forever client build 1.60.1.70959 of 17 November. Builds 1.60.1.70790 and 1.60.1.70888, read on 12 November, carry the same values. The table also lists level 60 to 61, which does not apply while the level cap is 60.

| Level reached | Total XP from level 1 | Share of the XP to 60 |
| --- | --- | --- |
| 10 | 27,600 | 0.7% |
| 20 | 167,200 | 4.1% |
| 30 | 499,000 | 12.2% |
| 40 | 1,154,400 | 28.3% |
| 50 | 2,306,100 | 56.5% |
| 60 | 4,084,700 | 100% |

Levels 50 to 60 take 43.5% of the total. The XP per level matches Classic: Wowhead reported a reduced curve from datamined files on 21 September 2026 and later retracted it; Blizzard confirmed the amounts are unchanged. The full table with every level is in `data/xp-per-level.csv` and on the Realm First [XP per level page](https://realmfirst.net/world-of-warcraft-forever/leveling-guide/wow-forever-xp-per-level/?from=github-xp-data). Realm First has not timed any of this in the game.

## When does WoW Forever launch

Blizzard says the game "launches globally on November 4, 2026, at 3:00 p.m. PST", which is 23:00 UTC. Blizzard gives one hour for every region, so each row below converts that one moment. The offsets are the ones in force on November 4: US daylight saving time ends on November 1 and Europe's ended on October 25, so both sit on standard time, and Sydney is on summer time.

| Time zone | Offset on November 4 | Launch time |
| --- | --- | --- |
| Pacific (PST) | UTC−8 | Wednesday, November 4, 3:00 p.m. |
| Central US (CST) | UTC−6 | Wednesday, November 4, 5:00 p.m. |
| Eastern US (EST) | UTC−5 | Wednesday, November 4, 6:00 p.m. |
| UTC | UTC+0 | Wednesday, November 4, 23:00 |
| UK and Ireland (GMT) | UTC+0 | Wednesday, November 4, 23:00 |
| Central Europe, including Vienna (CET) | UTC+1 | Thursday, November 5, 00:00 |
| Tokyo (JST) | UTC+9 | Thursday, November 5, 08:00 |
| Sydney (AEDT) | UTC+11 | Thursday, November 5, 10:00 |

Source: Blizzard Entertainment, [Pre-Purchase World of Warcraft: Forever Upgrades and Begin Your Next Journey in Azeroth](https://news.blizzard.com/en-us/article/24301508/pre-purchase-world-of-warcraft-forever-upgrades-and-begin-your-next-journey-in-azeroth), published September 12, 2026 and read again on October 29, 2026. Blizzard's posts give no regional openings and do not say whether servers or the client open earlier. The [Realm First start page](https://realmfirst.net/start-here/?from=github-launch-data) carries the same moment for more regions, and `data/launch-times.csv` includes those rows.

## Is WoW Forever a private server

No. World of Warcraft: Forever is Blizzard's own game: Blizzard announced it and its pre-purchase upgrades on its own news site (source: the Blizzard post above). A private server is a third-party emulation of the game; Forever runs on Blizzard's Forever client, which is also why an addon needs a build for that client. Source for the client: the Realm First [addons page](https://realmfirst.net/world-of-warcraft-forever/addons/?from=github-launch-data), checked 27 October 2026.

## Addon status at launch

- Questie, Guidelime, RestedXP Guides, BigWigs, Deadly Boss Mods, Plater and Bartender4 each list a Forever build (Interface 16001) in their latest GitHub release.
- WeakAuras lists none: release 5.22.1 of 10 October names other game flavors and no Forever flavor.
- Guidelime requires Questie on Forever. RestedXP Guides lists Questie only as optional.
- Realm First has not run these addons on a Forever client, so a listed build says nothing about features.
- Source and date: the Realm First [addons page](https://realmfirst.net/world-of-warcraft-forever/addons/?from=github-launch-data), read from the GitHub releases on 27 October 2026.

## Files

- `data/xp-per-level.csv` has the columns `level`, `next_level`, `xp_to_next_level`, `total_xp_at_next_level`, `client_build`, `source_url` and `retrieved`. One row per level step from 1 to 2 up to 59 to 60; `total_xp_at_next_level` adds the steps up from level 1.
- `data/launch-times.csv` has the columns `zone`, `utc_offset_on_launch_day`, `local_date`, `local_time` and `source_url`. The launch moment is 2026-11-04 23:00 UTC. Dates are ISO dates and times are 24-hour local clock times. Offsets for the rows taken from the Realm First start page are computed from that moment.
- `data/sources.csv` has the columns `id`, `title`, `publisher`, `url`, `published`, `retrieved`. `published` is the date the source gives, or the date it was last updated. `retrieved` is the day the desk read it.

## How to cite

Realm First News Desk. "WoW Forever launch data". Version 2, 2026-11-20. https://github.com/realmfirst/wow-forever-launch-data

GitHub reads the same line from `CITATION.cff` ("Cite this repository"). To cite one table, add its file, for example `data/xp-per-level.csv`.

## License

The data and text in this repository are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

Prepared with AI assistance by the Realm First desk; every row carries its source. Launch data checked on 29 October 2026, XP table on 20 November 2026.
