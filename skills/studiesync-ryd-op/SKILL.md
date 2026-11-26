---
name: studiesync-ryd-op
description: Læg filerne i mappen "Generelt" i et StudieSync-fag i de rigtige emne- eller ugemapper, først efter elevens ja. Bruges ved "ryd op", "sortér mine filer" eller "læg filerne i mapper" i et fag (tidy up, sort my files).
---

# Ryd op i et StudieSync-fag

Eleven vil have filerne i fagets mappe "Generelt" lagt i de rigtige mapper, fx "Ryd op i Statistik".

## Sådan gør du

1. Kald `list_courses`, og find faget ud fra elevens ord. Findes det ikke, så vis eleven sine fag, og spørg.
2. Kald `list_own_files` for faget, og find filerne i mappen "Generelt".
3. Find for hver fil den emne- eller ugemappe i faget, den hører til, ud fra filens navn og fagets mapper. Er du i tvivl om en fil, så lad den blive, og sig det.
4. Vis eleven planen først: hver fil og hvortil den skal.
5. Flyt først med `move_file`, når eleven siger ja. Siger eleven ja til en del af planen, så flyt kun den del.

## Regler

- Slet aldrig noget, og omdøb intet.
- Har du ikke `list_own_files` og `move_file`, så sig til eleven, at sortering ikke er slået til for StudieSync-forbindelsen endnu, og stop.
- Svar på det sprog, eleven skriver på.
