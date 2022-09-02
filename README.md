# Emu⬅re➡lation
Emu⬅re➡lation is project with 1 simple purpose; to provide a mapping of platforms, emulators, and games between varied sources in a easy to use JSON format.

## ❓ Why
There are many websites, programs, etc relating to emulation and many use entirely different names for the same thing.   This disparity adds difficulty to both the end user trying to play a game and developers.  We all have to deal with this in one way or another, and my goal with this project is to simplify and standardize that process.

## 🔀 What is being stored
The mapping data will consist of IDs and names while intentionally avoiding data or content beyond that such as descriptions and images.  This is to avoid any of the sources we are linking from feeling like we are stealing thier data or circumventing them.  I hope to make everyones life a little easier, eventually.

## 🔄 Status

The _Platform_ matches are finished/usable.  The _Emulators_ and _Companies_ matching will be added shortly.  After that I'll make the first release and announce the project.  Later on the _Games_ matches will get added.

## 🔃 Contributing
All contributions (issues, comments, pull requests, etc) are welcomed and encouraged.  If you have any projects using or relating to this repo let me know and I can add a link to it.

## 📂 Mapping Files

| File | Description |
|-|-|
| [sources.json](sources.json) | list of sources |
| [local.json](local.json) | local platform list with maches to the other sources |
| [sources/*.json](sources/) | each sources list of ids+names |

## 🗺 Supported Mapping

### 🎮 Platforms

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [LaunchBox](sources/launchbox.json) | Frontend | 194 | 0 | 194 | 100% |
| [MAME](sources/mame.json) | Emulator | 623 | 46 | 669 | 93.1% |
| [No-Intro](sources/nointro.json) | DAT | 253 | 31 | 284 | 89.1% |
| [Old-Computers](sources/oldcomputers.json) | Website | 164 | 1124 | 1288 | 12.7% |
| [Redump](sources/redump.json) | DAT | 50 | 1 | 51 | 98% |
| [ScreenScraper](sources/screenscraper.json) | API | 157 | 73 | 230 | 68.3% |
| [TheGamesDB](sources/tgdb.json) | API | 137 | 10 | 147 | 93.2% |
| [TOSEC](sources/tosec.json) | DAT | 2788 | 32 | 2820 | 98.9% |
| [TOSEC-ISO](sources/toseciso.json) | DAT | 242 | 0 | 242 | 100% |
| [TOSEC-PIX](sources/tosecpix.json) | DAT | 663 | 218 | 881 | 75.3% |

### 💾 Emulators
To be added soon

### 🏭 Companies
To be added soon

### 🕹 Games
Wont have these mapped for a while yet

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
  - emuControlCenter
  - EmulationKing
  - EmuCR
  - EmuTopia
  - EmuParadise
  - HyperSpin
  - RecalBox
  - RetroPie
  - MobyGames
  - IGDB

### 🔁 Schemas and Data Definitions
- Source Definitions list will define each source with (* required):
  - id*
  - name*
  - type*
  - description
  - provides[]*
  - updatedLast
  - updateTrigger
  - web<url, name>
- Source Data will have (* required):
  - platforms<>
    - id*
    - name*
    - shortName (dirname)
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
    - matches[source][id]
  - emulators<>
    - id*
    - name*
    - platforms[]
    - matches[source][id]
  - games<>
    - id*
    - name*
    - platform*
    - matches[source][id]
