# Emu⬅re➡lation

EmuRelation is project with 1 simple purpose; to provide a mapping of platforms, emulators, and games between varied sources in a easy to use JSON format.

## ❓ Why

There are many websites, programs, etc relating to emulation and many use entirely different names for the same thing.   This disparity adds difficulty to both the end user trying to play a game and developers.  We all have to deal with this in one way or another, and my goal with this project is to simplify and standardize that process.

## 🔀 What is being stored

The mapping data will consist of IDs and names while intentionally avoiding data or content beyond that such as descriptions and images.  This is to avoid any of the sources we are linking from feeling like we are stealing their data or circumventing them.  I hope to make every-ones life a little easier, eventually.

## 🗺 Supported Mapping

### 📂 Mapping Sources

- [sources.json](sources.json)

### 🎮 Platforms

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](platforms/local.json) | Custom | 795 | 0 | 795 | 100% |
| [Redump](platforms/redump.json) | DAT | 52 | 1 | 53 | 98.1% |
| [No-Intro](platforms/nointro.json) | DAT | 271 | 19 | 290 | 93.4% |
| [TOSEC](platforms/tosec.json) | DAT | 2427 | 1 | 2428 | 100% |
| [TOSEC-ISO](platforms/toseciso.json) | DAT | 241 | 0 | 241 | 100% |
| [TOSEC-PIX](platforms/tosecpix.json) | DAT | 634 | 227 | 861 | 73.6% |
| [TheGamesDB](platforms/tgdb.json) | API | 139 | 8 | 147 | 94.6% |
| [ScreenScraper](platforms/screenscraper.json) | API | 160 | 65 | 225 | 71.1% |
| [IGDB](platforms/igdb.json) | API | 80 | 0 | 80 | 100% |
| [HFS-DB](platforms/hfsdb.json) | API | 123 | 0 | 123 | 100% |
| [MobyGames](platforms/mobygames.json) | API | 110 | 0 | 110 | 100% |
| [Old-Computers](platforms/oldcomputers.json) | Website | 182 | 1104 | 1286 | 14.2% |
| [GameTDB](platforms/gametdb.json) | Website | 7 | 0 | 7 | 100% |
| [EmulationKing](platforms/emulationking.json) | Website | 34 | 0 | 34 | 100% |
| [Emutopia](platforms/emutopia.json) | Website | 90 | 85 | 175 | 51.4% |
| [MAME](platforms/mame.json) | Emulator | 649 | 15 | 664 | 97.7% |
| [LaunchBox](platforms/launchbox.json) | Frontend | 649 | 16 | 665 | 97.6% |
| [RetroBat](platforms/retrobat.json) | Frontend | 130 | 22 | 152 | 85.5% |
| [EmulationStation-DE](platforms/emulationstation-de.json) | Frontend | 135 | 21 | 156 | 86.5% |
| [RecalBox](platforms/recalbox.json) | Frontend | 98 | 28 | 126 | 77.8% |
| [RetroPie](platforms/retropie.json) | Frontend | 76 | 6 | 82 | 92.7% |
| [WinDSPro](platforms/windspro.json) | Frontend | 15 | 36 | 51 | 29.4% |
| [ARRM](platforms/arrm.json) | Tools | 213 | 62 | 275 | 77.5% |
| [emuControlCenter](platforms/emucontrolcenter.json) | Tools | 175 | 22 | 197 | 88.8% |

### 💾 Emulators

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](emulators/local.json) | Custom | 756 | 0 | 756 | 100% |
| [ScreenScraper](emulators/screenscraper.json) | API | 3 | 0 | 3 | 100% |
| [Old-Computers](emulators/oldcomputers.json) | Website | 116 | 350 | 466 | 24.9% |
| [EmulationKing](emulators/emulationking.json) | Website | 96 | 0 | 96 | 100% |
| [Emutopia](emulators/emutopia.json) | Website | 227 | 302 | 529 | 42.9% |
| [LaunchBox](emulators/launchbox.json) | Frontend | 30 | 0 | 30 | 100% |
| [RetroBat](emulators/retrobat.json) | Frontend | 0 | 0 | 0 | 0% |
| [EmulationStation-DE](emulators/emulationstation-de.json) | Frontend | 161 | 6 | 167 | 96.4% |
| [RecalBox](emulators/recalbox.json) | Frontend | 159 | 0 | 159 | 100% |
| [RetroPie](emulators/retropie.json) | Frontend | 152 | 1 | 153 | 99.3% |
| [WinDSPro](emulators/windspro.json) | Frontend | 82 | 9 | 91 | 90.1% |
| [emuControlCenter](emulators/emucontrolcenter.json) | Tools | 490 | 0 | 490 | 100% |
| [scoop-emulators](emulators/scoop-emulators.json) | Tools | 95 | 37 | 132 | 72% |

### 🏭 Companies

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](companies/local.json) | Custom | 287 | 0 | 287 | 100% |
| [ScreenScraper](companies/screenscraper.json) | API | 28 | 28 | 56 | 50% |
| [Old-Computers](companies/oldcomputers.json) | Website | 114 | 527 | 641 | 17.8% |
| [EmulationKing](companies/emulationking.json) | Website | 5 | 0 | 5 | 100% |
| [LaunchBox](companies/launchbox.json) | Frontend | 44 | 81 | 125 | 35.2% |
| [RecalBox](companies/recalbox.json) | Frontend | 31 | 22 | 53 | 58.5% |
| [ARRM](companies/arrm.json) | Tools | 50 | 14 | 64 | 78.1% |
| [emuControlCenter](companies/emucontrolcenter.json) | Tools | 75 | 23 | 98 | 76.5% |

### 🕹 Games

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](games/local.json) | Custom | 0 | 0 | 0 | 0% |
| [ScreenScraper](games/screenscraper.json) | API | 0 | 0 | 0 | 0% |
| [GameTDB](games/gametdb.json) | Website | 0 | 0 | 0 | 0% |
| [LaunchBox](games/launchbox.json) | Frontend | 0 | 0 | 0 | 0% |
| [emuControlCenter](games/emucontrolcenter.json) | Tools | 0 | 58143 | 58143 | 0% |

## 📒 Development Notes

- Source file generation and is currently done by scripts in [ConSolo](https://github.com/detain/ConSolo) project, but will likely be moving that.
- [emurelator](https://github.com/detain/emurelator) is a CLI for management of the information but is in early development.
- Local platforms
  - should come from sources that supply the actual games/roms (No-Intro, TOSEC, Redump, MAME) to ensure we have whats needed without going too overboard:
  - should be a single platform rather than several unless all sources also group them.  This should help ensure ideal mapping.  For example, having "Thomson MO5, MO6, and MO7" vs "Thomson MO5", "Thomson MO6", and "Thomson MO7" platforms.
- IDs should match the ID/Name used by the source.  An example from a TOSEC DAT is "Acorn BBC - Games - [DSD]".  While I could code in parsers and narrow it to say "Acorn BBC", I feel sticking with IDs that exactly match what the source uses for an entry will make it easier for people utilizing this information. If a more specific or alternate name is calculated, then it should be used in the AltNames[] section.

### ☑ TODO

- Ensure utf8/foreign/etc characters are supported and getting through, such as " and '
- Setup source exports for
  - Frontends
    - HyperSpin
    - EmulationStation
    - RetroArch
    - RetroBat
  - APIs
    - MobyGames
    - IGDB
    - HFS-DB
    - GamesTDB
  - Tools
    - skeletonKey
  - Websites
    - GamesDatabase
    - EmuCR
    - EmuTopia
    - EmuParadise
    - SegaRetro.org
    - Emulator.Games
    - emulator-zone.com
    - emulation64.com
    - emulationrealm.net
    - zophar.net

## 🔃 Contributing

All contributions (issues, comments, pull requests, etc) are welcomed and encouraged.  If you have any projects using or relating to this repo let me know and I can add a link to it.

## 🔁 Schemas and Data Definitions

_fields ending in * are required_

- Source Definitions list will define each source with
  - id*
  - name*
  - type*
  - description
  - provides[]*
  - updatedLast
  - updateTrigger
  - web<url, name>
- Source Data will have
  - platforms<>
    - id*
    - name*
    - shortName
    - company
    - manufacturer
    - developer
    - altNames[]
    - images<url,type>
    - web<url, name>
    - matches[source][id]
  - companies<>
    - id*
    - name*
    - shortName
    - matches[source][id]
  - emulators<>
    - id*
    - name*
    - shortName
    - platforms[]
    - matches[source][id]
  - games<>
    - id*
    - name*
    - shortName
    - platform*
    - matches[source][id]
