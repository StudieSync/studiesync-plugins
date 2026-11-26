---
name: studiesync-eksamen
description: Eksamenssparring ét spørgsmål ad gangen med feedback ud fra elevens StudieSync-filer i et fag eller en uge. Bruges ved "eksamen", "træn mig" eller "eksamenstræning" om et fag (exam practice, train me for the exam).
---

# Eksamenssparring i et StudieSync-fag

Eleven vil trænes til eksamen i en uge eller et emne i et af sine fag, fx "Træn mig til eksamen i Statistik uge 48".

## Find filerne

1. Kald `list_courses`, og find faget ud fra elevens ord (fagets kode, navn eller `course_id`). Findes faget ikke, så vis eleven sine fag fra `list_courses`, og spørg, hvilket der menes.
2. Kald `list_files` for faget, og find modulet eller ugen, eleven nævner. Nævner eleven ingen uge, så vælg det modul, der passer til denne uge, og skriv, hvilket du valgte. Findes ugen eller emnet ikke, så vis fagets moduler, og spørg.
3. Åbn modulets filer via deres Google Drev-links med din egen Google Drev-forbindelse, og læs dem, før du svarer. StudieSync sender aldrig selv filindhold, kun links. Kan du ikke åbne filerne, så sig det, og bed eleven forbinde Google Drev i netop denne AI-app, i stedet for at gætte. Har modulet ingen filer, du kan læse, så sig det, og foreslå et andet emne fra `list_files`.

## Sådan træner du eleven

- Stil ét eksamensagtigt spørgsmål ad gangen, og vent på elevens svar.
- Giv derefter feedback: hvad var rigtigt, hvad manglede, og hvor i filerne det står.
- Gør spørgsmålene sværere, når eleven svarer godt, og lettere, når eleven er usikker.
- Efter fem spørgsmål opsummerer du, hvad eleven skal læse op på.

Start med det første spørgsmål, så snart du har læst filerne.

## Regler

- Svar ud fra filerne, og henvis til fil og side eller slide. Dækker filerne ikke et punkt, så skriv det i stedet for at gætte.
- Materialet tilhører underviserne og universitetet: citér kun det nødvendige, og giv det ikke videre.
- Svar på det sprog, eleven skriver på.

## Gem resultatet

Når du er færdig, så spørg eleven, om resultatet skal gemmes. Kun ved ja kalder du `create_note` med fagets `course_id`, en kort titel og hele noten som Markdown i `text`. Lav ikke selv filer i elevens Drev. Har du ikke `create_note`, så spring dette trin over.
