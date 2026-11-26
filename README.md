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

## What the connector's tools can do

The plugin brings one server, the StudieSync connector. It only works inside the signed-in student's own StudieSync courses and their own Google Drive. Its tools:

- **Read:** `list_courses`, `list_files` and `list_own_files` list your courses, topics, file names and links to your own Drive.
- **Create and save:** `create_note` saves a new note (as a Google Doc) and `create_file` saves a new file (at most 5 MB, no programs) in a course folder in your Google Drive. `create_folder` makes a new folder in a course.
- **Move and rename:** `move_file` and `move_folder` move your files and folders between the folders of one course. `rename` renames your own files, notes and folders.
- **Delete:** `delete` moves one of your own files or notes to the bin of your Google Drive, where you can restore it for 30 days, and deletes an empty folder of your own. Canvas files can never be renamed or deleted.

None of the tools send, publish or share anything with other people, take payments or change who has access to anything. The skills tell Claude to show you its plan and wait for your yes before it saves, moves, renames or deletes anything.

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

StudieSync never sends your course files' contents to Claude. The connector only shares course names, topics, file names and links to your own Google Drive; Claude opens the files with its own Google Drive connection. A note or file Claude saves for you is passed straight on to your own Google Drive and never stored by StudieSync. The skills are fixed texts and hold nothing about you.

Support: info@studiesync.dk · Privacy policy: https://app.studiesync.dk/privatlivspolitik
