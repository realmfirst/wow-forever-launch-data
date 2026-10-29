# WoW Forever launch data

This repository holds the launch time of World of Warcraft: Forever by time zone, the answer to whether it is a private server, and the addon status at launch, prepared with AI assistance by the Realm First desk. Every row names its source.

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

- `data/launch-times.csv` has the columns `zone`, `utc_offset_on_launch_day`, `local_date`, `local_time` and `source_url`. The launch moment is 2026-11-04 23:00 UTC. Dates are ISO dates and times are 24-hour local clock times. Offsets for the rows taken from the Realm First start page are computed from that moment.
- `data/sources.csv` has the columns `id`, `title`, `publisher`, `url`, `published`, `retrieved`. `published` is the date the source gives, or the date it was last updated. `retrieved` is the day the desk read it.

## How to cite

Realm First desk. "WoW Forever launch data". Version 1, 2026-10-29. https://github.com/realmfirst/wow-forever-launch-data

## License

The data and text in this repository are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

Prepared with AI assistance by the Realm First desk; every row carries its source. Checked on 29 October 2026.
