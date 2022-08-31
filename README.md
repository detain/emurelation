# Emu⬅re➡lation
Emu⬅re➡lation is project with 1 simple purpose; to provide a mapping in JSON format of platforms, emulators, and related inforamtion accross different sources.  There are several varied naming conventions used and many different programs and sites and this aims to allow you an easy way to convert or map the data from one type to another.

## Status

Currently undergoing restructuring and finishing scripts to generate the remaining source files.  After that I'll update the matches using the new files and finish up the matching data.  After which we should be ready for the first release.


### Dev Notes

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

##### TODO

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

| Source | Platforms | Matched | Missing | % Completed |
|--|--|--|--|--|
| Master List | 717 | 0 | 717 | 0% |
| TOSEC | 413 | 359 | 54 | 86.9% |
| No-Intro | 135 | 92 | 43 | 68.1% |
| Redump | 51 | 45 | 6 | 88.2% |
| MAME | 544 | 491 | 53 | 90.3% |
| LaunchBox | 183 | 183 | 0 | 100% |
| TheGamesDB | 114 | 75 | 39 | 65.8% |
| ScreenScraper.fr | 223 | 113 | 110 | 50.7% |
| Old-Computers.com | 1278 | 90 | 1188 | 7% |
