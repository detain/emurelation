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
| [Local](platforms/local.json) | Custom | 883 | 0 | 883 | 100% |
| [Redump](platforms/redump.json) | DAT | 52 | 1 | 53 | 98.1% |
| [No-Intro](platforms/nointro.json) | DAT | 271 | 19 | 290 | 93.4% |
| [TOSEC](platforms/tosec.json) | DAT | 2427 | 1 | 2428 | 100% |
| [TOSEC-ISO](platforms/toseciso.json) | DAT | 241 | 0 | 241 | 100% |
| [TOSEC-PIX](platforms/tosecpix.json) | DAT | 634 | 227 | 861 | 73.6% |
| [TheGamesDB](platforms/tgdb.json) | API | 139 | 8 | 147 | 94.6% |
| [ScreenScraper](platforms/screenscraper.json) | API | 226 | 0 | 226 | 100% |
| [IGDB](platforms/igdb.json) | API | 80 | 0 | 80 | 100% |
| [HFS-DB](platforms/hfsdb.json) | API | 124 | 0 | 124 | 100% |
| [MobyGames](platforms/mobygames.json) | API | 111 | 0 | 111 | 100% |
| [Old-Computers](platforms/oldcomputers.json) | Website | 201 | 1085 | 1286 | 15.6% |
| [GameTDB](platforms/gametdb.json) | Website | 7 | 0 | 7 | 100% |
| [EmulationKing](platforms/emulationking.json) | Website | 34 | 0 | 34 | 100% |
| [Emutopia](platforms/emutopia.json) | Website | 143 | 32 | 175 | 81.7% |
| [MAME](platforms/mame.json) | Emulator | 649 | 15 | 664 | 97.7% |
| [LaunchBox](platforms/launchbox.json) | Frontend | 649 | 16 | 665 | 97.6% |
| [RetroBat](platforms/retrobat.json) | Frontend | 139 | 13 | 152 | 91.4% |
| [EmulationStation-DE](platforms/emulationstation-de.json) | Frontend | 144 | 12 | 156 | 92.3% |
| [RecalBox](platforms/recalbox.json) | Frontend | 105 | 21 | 126 | 83.3% |
| [RetroPie](platforms/retropie.json) | Frontend | 80 | 2 | 82 | 97.6% |
| [WinDSPro](platforms/windspro.json) | Frontend | 15 | 36 | 51 | 29.4% |
| [ARRM](platforms/arrm.json) | Tools | 224 | 51 | 275 | 81.5% |
| [emuControlCenter](platforms/emucontrolcenter.json) | Tools | 177 | 20 | 197 | 89.8% |

### 💾 Emulators

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](emulators/local.json) | Custom | 826 | 0 | 826 | 100% |
| [ScreenScraper](emulators/screenscraper.json) | API | 3 | 1 | 4 | 75% |
| [Old-Computers](emulators/oldcomputers.json) | Website | 149 | 317 | 466 | 32% |
| [EmuCR](emulators/emucr.json) | Website | 339 | 2002 | 2341 | 14.5% |
| [EmulationKing](emulators/emulationking.json) | Website | 96 | 0 | 96 | 100% |
| [Emutopia](emulators/emutopia.json) | Website | 246 | 283 | 529 | 46.5% |
| [LaunchBox](emulators/launchbox.json) | Frontend | 30 | 0 | 30 | 100% |
| [RetroBat](emulators/retrobat.json) | Frontend | 0 | 0 | 0 | 0% |
| [EmulationStation-DE](emulators/emulationstation-de.json) | Frontend | 161 | 6 | 167 | 96.4% |
| [RecalBox](emulators/recalbox.json) | Frontend | 159 | 0 | 159 | 100% |
| [RetroPie](emulators/retropie.json) | Frontend | 152 | 1 | 153 | 99.3% |
| [WinDSPro](emulators/windspro.json) | Frontend | 82 | 9 | 91 | 90.1% |
| [emuControlCenter](emulators/emucontrolcenter.json) | Tools | 490 | 0 | 490 | 100% |
| [scoop-emulators](emulators/scoop-emulators.json) | Tools | 612 | 12 | 624 | 98.1% |

### 🏭 Companies

| Source | Type | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|-|
| [Local](companies/local.json) | Custom | 312 | 0 | 312 | 100% |
| [ScreenScraper](companies/screenscraper.json) | API | 52 | 4 | 56 | 92.9% |
| [Old-Computers](companies/oldcomputers.json) | Website | 114 | 527 | 641 | 17.8% |
| [EmulationKing](companies/emulationking.json) | Website | 5 | 0 | 5 | 100% |
| [LaunchBox](companies/launchbox.json) | Frontend | 45 | 80 | 125 | 36% |
| [RecalBox](companies/recalbox.json) | Frontend | 31 | 22 | 53 | 58.5% |
| [ARRM](companies/arrm.json) | Tools | 51 | 13 | 64 | 79.7% |
| [emuControlCenter](companies/emucontrolcenter.json) | Tools | 76 | 22 | 98 | 77.6% |

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

- Match up all the local Emulators with their respective Platforms
- Check other buckets for matching emulators and compair to see if there are things ii can improve
- Check other buckets for missing emulators and add any appropriate ones
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
    - EmuParadise
    - SegaRetro.org
    - Emulator.Games
    - emulator-zone.com
    - emulation64.com
    - emulationrealm.net
    - zophar.net

### Buckets to check out

* [ACooper81/scoop-apps](ACooper81/scoop-apps)
* [borger/scoop-emulators](borger/scoop-emulators)
* [Calinou/scoop-games](Calinou/scoop-games)
* [cc713/ownscoop](cc713/ownscoop)
* [dschaefer/scoop-tools816](dschaefer/scoop-tools816)
* [hermanjustnu/scoop-emulators](hermanjustnu/scoop-emulators)
* [HUMORCE/nuke](HUMORCE/nuke)
* [Inari-Whitebear/scoopBucket](Inari-Whitebear/scoopBucket)
* [littleli/Scoop-AtariEmulators](littleli/Scoop-AtariEmulators)
* [littleli/scoop-games](littleli/scoop-games)
* [littleli/scoop-garage](littleli/scoop-garage)
* [Notenoughusernames/bluemoon](Notenoughusernames/bluemoon)
* [ProfElements/EmulatorBucket](ProfElements/EmulatorBucket)
* [p8rdev/scoop-portableapps](p8rdev/scoop-portableapps)
* [ScoopInstaller/Extras](ScoopInstaller/Extras)
* [ScoopInstaller/Main](ScoopInstaller/Main)
* [ScoopInstaller/Nonportable](ScoopInstaller/Nonportable)
* [ScoopInstaller/PHP](ScoopInstaller/PHP)
* [ScoopInstaller/Versions](ScoopInstaller/Versions)
* [TheRandomLabs/scoop-nonportable](TheRandomLabs/scoop-nonportable)

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
