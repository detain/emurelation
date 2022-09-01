# Emu⬅re➡lation
Emu⬅re➡lation is project with 1 simple purpose; to provide a mapping of platforms, emulators, and games between varied sources in a easy to use JSON format.

## ❓ Why
There are many websites, programs, etc relating to emulation and many use entirely different names for the same thing.   This disparity adds difficulty to both the end user trying to play a game and developers.  We all have to deal with this in one way or another, and my goal with this project is to simplify and standardize that process.

## 🔀 What is being stored
The mapping data will consist of IDs and names while intentionally avoiding data or content beyond that such as descriptions and images.  This is to avoid any of the sources we are linking from feeling like we are stealing thier data or circumventing them.  I hope to make everyones life a little easier, eventually.

## 🔄 Status
Currently undergoing restructuring and finishing scripts to generate the remaining source files.  After that I'll update the matches using the new files and finish up the matching data.  After which we should be ready for the first release.

## 🔃 Contributing
All contributions (issues, comments, pull requests, etc) are welcomed and encouraged.  If you have any projects using or relating to this repo let me know and I can add a link to it.

## 📂 Mapping Files

| File | Description |
|-|-|
| [sources.json](sources.json) | list of sources |
| [sources/local.json](sources/local.json) | local platform list with maches to the other sources |
| [sources/*.json](sources/) | each sources list of ids+names |
| [matches/*.json](matches/) | old matching files, will be phased out |
| [linker.json](linker.json) | old matching file, will be phased out |
| [platforms.json](platforms.json) | old matching file, will be phased out |

## 🗺 Supported Mapping

### 🎮 Platforms

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [LaunchBox](sources/launchbox.json) | Frontend | 183 | 0 | 183 | 100% |
| [MAME](sources/mame.json) | Emulator | 618 | 42 | 660 | 93.6% |
| [No-Intro](sources/nointro.json) | DAT | 246 | 38 | 284 | 86.6% |
| [Old-Computers](sources/oldcomputers.json) | Website | 111 | 1175 | 1286 | 8.6% |
| [Redump](sources/redump.json) | DAT | 50 | 1 | 51 | 98% |
| [ScreenScraper](sources/screenscraper.json) | API | 148 | 77 | 225 | 65.8% |
| [TheGamesDB](sources/tgdb.json) | API | 133 | 14 | 147 | 90.5% |
| [TOSEC](sources/tosec.json) | DAT | 2388 | 40 | 2428 | 98.4% |
| [TOSEC-ISO](sources/toseciso.json) | DAT | 241 | 0 | 241 | 100% |
| [TOSEC-PIX](sources/tosecpix.json) | DAT | 642 | 219 | 861 | 74.6% |

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
  - should come from sources that supply the actual games/roms to ensure we have whats needed without going too overboard:
    - No-Intro
    - TOSEC
    - Redump
    - MAME
  - should be a single platform rather than several unless all sources also group them.  This should help ensure ideal mapping.  ie having "Thomson MO5, MO6, and MO7" vs "Thomson MO5", "Thomson MO6", and "Thomson MO7" platforms
- IDs should match the ID/Name used by the source.  An example from a TOSEC DAT is "Acorn BBC - Games - [DSD]".  While I could code in parsers and narrow it to say "Acorn BBC", I feel sticking with IDs that exactly match what the source uses for an entry will make it easier for people utilizing this information.

### ☑ TODO
- Add local platforms for any unmatched nointro/redump/tosec/mame sources
- Possibly drop description from source exports
- remove excess local platforms without at least 1 nointro/redump/tosec/mame match
- Ensure utf8/foreign/etc characters are supported and getting through, such as " and '
- Setup source exports for
  - LaunchBox emulators
  - emuControlCenter
  - EmulationKing
  - EmuCR
  - EmuTopia
  - EmuParadise
  - HyperSpin
  - RecalBox
  - RetroPie

### 🔁 Schemas and Data Definitions
- Types to match between sources:
  - Companies
  - Platforms
  - Emulators
  - Games
- Sources list will define each source with (* required):
  - id*
  - name*
  - type*
  - info
  - provides[]*
  - updatedLast
  - updateTrigger
  - web<url, name>
- each Source will have (* required):
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

