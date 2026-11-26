---
name: studiesync-overblik
description: Giv et overblik over en uge eller et emne i et af elevens StudieSync-fag ud fra fagets egne filer. Bruges når eleven beder om overblik, et resumé eller "hvad handler uge N om" i et fag (overview, summary, what is week N about).
---

# Overblik over en uge i et StudieSync-fag

Eleven vil have et overblik over en uge eller et emne i et af sine fag, fx "Giv mig overblik over Statistik uge 48".

## Find filerne

1. Kald `list_courses`, og find faget ud fra elevens ord (fagets kode, navn eller `course_id`). Findes faget ikke, så vis eleven sine fag fra `list_courses`, og spørg, hvilket der menes.
2. Kald `list_files` for faget, og find modulet eller ugen, eleven nævner. Nævner eleven ingen uge, så vælg det modul, der passer til denne uge, og skriv, hvilket du valgte. Findes ugen eller emnet ikke, så vis fagets moduler, og spørg.
3. Åbn modulets filer via deres Google Drev-links med din egen Google Drev-forbindelse, og læs dem, før du svarer. StudieSync sender aldrig selv filindhold, kun links. Kan du ikke åbne filerne, så sig det, og bed eleven forbinde Google Drev i netop denne AI-app, i stedet for at gætte. Har modulet ingen filer, du kan læse, så sig det, og foreslå et andet emne fra `list_files`.

## Lav overblikket

Giv eleven:

1. De 3-5 vigtigste pointer, hver med henvisning til fil og side eller slide.
2. De centrale begreber, med en forklaring på én linje hver.
3. Hvordan emnet hænger sammen med det, faget har handlet om indtil nu.
4. Tre spørgsmål, eleven bør kunne svare på, når ugen er slut.

## Regler

- Svar ud fra filerne, og henvis til fil og side eller slide. Dækker filerne ikke et punkt, så skriv det i stedet for at gætte.
- Materialet tilhører underviserne og universitetet: citér kun det nødvendige, og giv det ikke videre.
- Svar på det sprog, eleven skriver på.

## Gem resultatet

Når du er færdig, så spørg eleven, om resultatet skal gemmes. Kun ved ja kalder du `create_note` med fagets `course_id`, en kort titel og hele noten som Markdown i `text`. Lav ikke selv filer i elevens Drev. Har du ikke `create_note`, så spring dette trin over.
