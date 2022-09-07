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
| [Local](sources/local.json) | Custom | 830 | 0 | 830 | 100% |
| [Redump](sources/redump.json) | DAT | 50 | 1 | 51 | 98% |
| [No-Intro](sources/nointro.json) | DAT | 256 | 28 | 284 | 90.1% |
| [TOSEC](sources/tosec.json) | DAT | 2788 | 32 | 2820 | 98.9% |
| [TOSEC-ISO](sources/toseciso.json) | DAT | 242 | 0 | 242 | 100% |
| [TOSEC-PIX](sources/tosecpix.json) | DAT | 663 | 218 | 881 | 75.3% |
| [TheGamesDB](sources/tgdb.json) | API | 139 | 8 | 147 | 94.6% |
| [ScreenScraper](sources/screenscraper.json) | API | 160 | 70 | 230 | 69.6% |
| [Old-Computers](sources/oldcomputers.json) | Website | 182 | 1106 | 1288 | 14.1% |
| [EmulationKing](sources/emulationking.json) | Website | 34 | 0 | 34 | 100% |
| [MAME](sources/mame.json) | Emulator | 628 | 41 | 669 | 93.9% |
| [LaunchBox](sources/launchbox.json) | Frontend | 194 | 0 | 194 | 100% |
| [EmulationStation-DE](sources/emulationstation-de.json) | Frontend | 126 | 30 | 156 | 80.8% |
| [RecalBox](sources/recalbox.json) | Frontend | 91 | 35 | 126 | 72.2% |
| [RetroPie](sources/retropie.json) | Frontend | 71 | 13 | 84 | 84.5% |
| [emuControlCenter](sources/emucontrolcenter.json) | Tools | 170 | 27 | 197 | 86.3% |

### 💾 Emulators

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](sources/local.json) | Custom | 490 | 0 | 490 | 100% |
| [ScreenScraper](sources/screenscraper.json) | API | 0 | 3 | 3 | 0% |
| [Old-Computers](sources/oldcomputers.json) | Website | 115 | 351 | 466 | 24.7% |
| [EmulationKing](sources/emulationking.json) | Website | 73 | 23 | 96 | 76% |
| [LaunchBox](sources/launchbox.json) | Frontend | 21 | 9 | 30 | 70% |
| [EmulationStation-DE](sources/emulationstation-de.json) | Frontend | 23 | 141 | 164 | 14% |
| [RecalBox](sources/recalbox.json) | Frontend | 12 | 147 | 159 | 7.5% |
| [RetroPie](sources/retropie.json) | Frontend | 25 | 128 | 153 | 16.3% |
| [emuControlCenter](sources/emucontrolcenter.json) | Tools | 490 | 0 | 490 | 100% |

### 🏭 Companies

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](sources/local.json) | Custom | 285 | 0 | 285 | 100% |
| [ScreenScraper](sources/screenscraper.json) | API | 28 | 28 | 56 | 50% |
| [Old-Computers](sources/oldcomputers.json) | Website | 114 | 527 | 641 | 17.8% |
| [EmulationKing](sources/emulationking.json) | Website | 5 | 0 | 5 | 100% |
| [LaunchBox](sources/launchbox.json) | Frontend | 45 | 80 | 125 | 36% |
| [RecalBox](sources/recalbox.json) | Frontend | 31 | 22 | 53 | 58.5% |
| [emuControlCenter](sources/emucontrolcenter.json) | Tools | 60 | 38 | 98 | 61.2% |

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

- Add local platforms for any unmatched nointro/redump/tosec/mame sources
- remove excess local platforms without at least 1 nointro/redump/tosec/mame match
- Ensure utf8/foreign/etc characters are supported and getting through, such as " and '
- Setup source exports for
  - Frontends
    - HyperSpin
    - EmulationStation
    - RetroArch
    - RetroBat
    - RecalBox
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
