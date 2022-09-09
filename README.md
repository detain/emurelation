# Emu⬅re➡lation

EmuRelation is project with 1 simple purpose; to provide a mapping of platforms, emulators, and games between varied sources in a easy to use JSON format.

## ❓ Why

There are many websites, programs, etc relating to emulation and many use entirely different names for the same thing.   This disparity adds difficulty to both the end user trying to play a game and developers.  We all have to deal with this in one way or another, and my goal with this project is to simplify and standardize that process.

## 🔀 What is being stored

The mapping data will consist of IDs and names while intentionally avoiding data or content beyond that such as descriptions and images.  This is to avoid any of the sources we are linking from feeling like we are stealing their data or circumventing them.  I hope to make every-ones life a little easier, eventually.

## 🗺 Supported Mapping

### 🎮 Platforms

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](sources/local.json) | Custom | 811 | 0 | 811 | 100% |
| [Redump](sources/redump.json) | DAT | 51 | 0 | 51 | 100% |
| [No-Intro](sources/nointro.json) | DAT | 266 | 18 | 284 | 93.7% |
| [TOSEC](sources/tosec.json) | DAT | 2821 | 1 | 2822 | 100% |
| [TOSEC-ISO](sources/toseciso.json) | DAT | 242 | 0 | 242 | 100% |
| [TOSEC-PIX](sources/tosecpix.json) | DAT | 654 | 227 | 881 | 74.2% |
| [TheGamesDB](sources/tgdb.json) | API | 139 | 8 | 147 | 94.6% |
| [ScreenScraper](sources/screenscraper.json) | API | 162 | 68 | 230 | 70.4% |
| [Old-Computers](sources/oldcomputers.json) | Website | 180 | 1108 | 1288 | 14% |
| [EmulationKing](sources/emulationking.json) | Website | 34 | 0 | 34 | 100% |
| [MAME](sources/mame.json) | Emulator | 654 | 15 | 669 | 97.8% |
| [LaunchBox](sources/launchbox.json) | Frontend | 194 | 0 | 194 | 100% |
| [EmulationStation-DE](sources/emulationstation-de.json) | Frontend | 134 | 22 | 156 | 85.9% |
| [RecalBox](sources/recalbox.json) | Frontend | 96 | 30 | 126 | 76.2% |
| [RetroPie](sources/retropie.json) | Frontend | 71 | 13 | 84 | 84.5% |
| [emuControlCenter](sources/emucontrolcenter.json) | Tools | 175 | 22 | 197 | 88.8% |

### 💾 Emulators

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](sources/local.json) | Custom | 772 | 0 | 772 | 100% |
| [ScreenScraper](sources/screenscraper.json) | API | 3 | 0 | 3 | 100% |
| [Old-Computers](sources/oldcomputers.json) | Website | 116 | 350 | 466 | 24.9% |
| [EmulationKing](sources/emulationking.json) | Website | 96 | 0 | 96 | 100% |
| [LaunchBox](sources/launchbox.json) | Frontend | 30 | 0 | 30 | 100% |
| [EmulationStation-DE](sources/emulationstation-de.json) | Frontend | 161 | 3 | 164 | 98.2% |
| [RecalBox](sources/recalbox.json) | Frontend | 159 | 0 | 159 | 100% |
| [RetroPie](sources/retropie.json) | Frontend | 153 | 0 | 153 | 100% |
| [emuControlCenter](sources/emucontrolcenter.json) | Tools | 490 | 0 | 490 | 100% |

### 🏭 Companies

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](sources/local.json) | Custom | 288 | 0 | 288 | 100% |
| [ScreenScraper](sources/screenscraper.json) | API | 28 | 28 | 56 | 50% |
| [Old-Computers](sources/oldcomputers.json) | Website | 114 | 527 | 641 | 17.8% |
| [EmulationKing](sources/emulationking.json) | Website | 5 | 0 | 5 | 100% |
| [LaunchBox](sources/launchbox.json) | Frontend | 44 | 81 | 125 | 35.2% |
| [RecalBox](sources/recalbox.json) | Frontend | 31 | 22 | 53 | 58.5% |
| [emuControlCenter](sources/emucontrolcenter.json) | Tools | 72 | 26 | 98 | 73.5% |

### 🕹 Games

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](sources/local.json) | Custom | 0 | 0 | 0 | 0% |
| [ScreenScraper](sources/screenscraper.json) | API | 0 | 0 | 0 | 0% |
| [LaunchBox](sources/launchbox.json) | Frontend | 0 | 0 | 0 | 0% |

### 📂 Mapping Files

| File | Description |
|-|-|
| [sources.json](sources.json) | list of sources |
| [local.json](local.json) | local/main listing providing matching between other sources |
| [sources/*.json](sources/) | each sources list of ids+names |

## 📒 Development Notes

- Source file generation and is currently done by scripts in [ConSolo](https://github.com/detain/ConSolo) project, but will likely be moving that.
- [emurelator](https://github.com/detain/emurelator) is a CLI for management of the information but is in early development.
- Local platforms
  - should come from sources that supply the actual games/roms (No-Intro, TOSEC, Redump, MAME) to ensure we have whats needed without going too overboard:
  - should be a single platform rather than several unless all sources also group them.  This should help ensure ideal mapping.  For example, having "Thomson MO5, MO6, and MO7" vs "Thomson MO5", "Thomson MO6", and "Thomson MO7" platforms.
- IDs should match the ID/Name used by the source.  An example from a TOSEC DAT is "Acorn BBC - Games - [DSD]".  While I could code in parsers and narrow it to say "Acorn BBC", I feel sticking with IDs that exactly match what the source uses for an entry will make it easier for people utilizing this information. If a more specific or alternate name is calculated, then it should be used in the AltNames[] section.

### ☑ TODO

- merge duplicate emulators in local list
- remove excess local platforms without at least 1 nointro/redump/tosec/mame match
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
  - Tools
    - skeletonKey
    - ARRM
  - Websites
    - EmuCR
    - EmuTopia
    - EmuParadise

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
