# Emu⬅re➡lation
Emu⬅re➡lation is project with 1 simple purpose; to provide a mapping in JSON format of platforms, emulators, and related inforamtion accross different sources.  There are several varied naming conventions used and many different programs and sites and this aims to allow you an easy way to convert or map the data from one type to another.

## Status

Currently undergoing restructuring and finishing scripts to generate the remaining source files.  After that I'll update the matches using the new files and finish up the matching data.  After which we should be ready for the first release.


## Dev Notes

- Main list of platforms should come from sources that supply the actual games/roms to ensure we have whats needed without going too overboard:
  - No-Intro
  - TOSEC
  - Redump
  - MAME
- Types to match between sources:
  - Companies
  - Platforms
  - Emulators
  - Games
- Sources list will define each source with (* required):
  - id*
  - name*
  - type*
  - provides[]*
  - info
  - updatedLast
  - updateTrigger
  - web<url, name>
- each Source will have (* required):
  - id*
  - name*
  - shortName (dirname)
  - description
  - company
  - manufacturer
  - developer
  - altNames[]
  - images<url,type>
  - web<url, name>
  - matches<source,id>

### TODO

- Update matches utilizing new source exports
- Possibly drop description from source exports
- Add local platforms for any unmatched nointro/redump/tosec/mame sources
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


## Supported Mapping

### Platforms

| Source | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|
| launchbox | 183 | 0 | 183 | 100% |
| mame | 597 | 63 | 660 | 90.5% |
| nointro | 181 | 103 | 284 | 63.7% |
| oldcomputers | 93 | 1193 | 1286 | 7.2% |
| redump | 50 | 1 | 51 | 98% |
| screenscraper | 116 | 108 | 224 | 51.8% |
| tgdb | 114 | 33 | 147 | 77.6% |
| tosec | 2322 | 106 | 2428 | 95.6% |
| toseciso | 241 | 0 | 241 | 100% |
| tosecpix | 561 | 300 | 861 | 65.2% |

### Emulators

To be added soon

### Companies

To be added soon

### Games

Wont have these mapped for a while yet

