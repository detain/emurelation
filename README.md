# Emu⬅re➡lation
Emu⬅re➡lation is project with 1 simple purpose; to provide a mapping in JSON format of platforms, emulators, and related inforamtion accross different sources.  There are several varied naming conventions used and many different programs and sites and this aims to allow you an easy way to convert or map the data from one type to another.

## Status

Currently undergoing restructuring and finishing scripts to generate the remaining source files.  After that I'll update the matches using the new files and finish up the matching data.  After which we should be ready for the first release.


## Mapping Files

| File | Description |
|-|-|
| sources.json | list of sources |
| sources/local.json | local platform list with maches to the other sources |
| sources/*.json | each sources list of ids+names |
| matches/*.json | old matching files, will be phased out |
| linker.json | old matching file, will be phased out |
| platforms.json | old matching file, will be phased out |

## Dev Notes

- Local platforms should come from sources that supply the actual games/roms to ensure we have whats needed without going too overboard:
  - No-Intro
  - TOSEC
  - Redump
  - MAME
- Local platforms should be a single platform rather than several unless all sources also group them.  This should help ensure ideal mapping.  ie having "Thomson MO5, MO6, and MO7" vs "Thomson MO5", "Thomson MO6", and "Thomson MO7" platforms
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
  - matches<source,id>

### TODO

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


## Supported Mapping

### Platforms

| Source | Mapped | Unmapped | Total | Mapped % |
|-|-|-|-|-|
| launchbox | 183 | 0 | 183 | 100% |
| mame | 600 | 60 | 660 | 90.9% |
| nointro | 221 | 63 | 284 | 77.8% |
| oldcomputers | 107 | 1179 | 1286 | 8.3% |
| redump | 50 | 1 | 51 | 98% |
| screenscraper | 145 | 79 | 224 | 64.7% |
| tgdb | 133 | 14 | 147 | 90.5% |
| tosec | 2326 | 102 | 2428 | 95.8% |
| toseciso | 241 | 0 | 241 | 100% |
| tosecpix | 642 | 219 | 861 | 74.6% |

### Emulators

To be added soon

### Companies

To be added soon

### Games

Wont have these mapped for a while yet

