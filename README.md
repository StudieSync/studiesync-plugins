# StudieSync for Claude

StudieSync syncs your Canvas courses into your own Google Drive, one folder per course and topic. This plugin connects Claude to the StudieSync connector (`https://app.studiesync.dk/mcp`) and adds six skills:

| Skill | Use it for |
|---|---|
| `studiesync-overblik` | An overview of a week or topic in a course |
| `studiesync-huskekort` | Flashcards from a course and week |
| `studiesync-quiz` | A multiple-choice quiz |
| `studiesync-eksamen` | Exam practice, one question at a time |
| `studiesync-forklar` | The hardest concepts explained simply |
| `studiesync-ryd-op` | Moving the files in "Generelt" into the right folders, after your yes |

Ask in your own words, for example "Lav huskekort til Statistik uge 48" or "Quiz me on week 3 in Microeconomics".

## Install

In Claude Code:

```
/plugin install studiesync --marketplace StudieSync/studiesync-plugins
```

In Claude (web, desktop and mobile), add StudieSync from the connector and plugin directory.

## Requirements

- A StudieSync account with Google Drive connected (https://studiesync.dk).
- Google Drive connected in Claude, so Claude can open the files.

## Privacy

StudieSync never sends file contents. The connector only shares course names, topics, file names and links to your own Google Drive; Claude opens the files with its own Google Drive connection. The skills are fixed texts and hold nothing about you.

Support: info@studiesync.dk · Privacy policy: https://app.studiesync.dk/privatlivspolitik
