# Changelog

## 0.2.8 — 2026-10-09

Version 0.2.7 → 0.2.8.

- Add initial tasks configuration to tasks.yaml
- Fix worker-thread double delete and hang on quit
- Pass Pandoc a local copy of the CSL style
- Refresh STATUS.md after merges and skip Windows-only tests off Windows
- Reorganize repository into folders and add direct installer link
- Add Zotero integration and enhance Word citation handling
- Implement background loading for library and project references
- feat: implement Zotero attachment migration plan and UI integration
- docs: record UGOS setup for phone tasks (ADR-013 step 7)
- feat: add phone task HTTP server (ADR-013 step 3)
- feat: add phone task page (ADR-013 step 4)
- feat: add NAS container files and setup guide for phone tasks (ADR-013 steps 5-6)
- docs: fix the phone task server contract before parallel work
- feat: add Qt-free task service for phone editing (ADR-013 step 2)
- docs: record that offline phone editing is not needed
- docs: propose phone task editing via NAS web server (ADR-013)
- feat: Update project metadata and structure in project.yaml

Drafted from commit messages by the publish workflow.

## 0.2.7 — 2026-10-08

Version 0.2.5 → 0.2.7.

### Changes in 0.2.7

- Projects → **Find moved projects…**: after moving many project folders at once,
  choose the folder they now live in. CALCIFER adds every project inside it, follows
  projects that moved there, and offers to forget old locations that no longer exist.
  No files are moved or deleted.
- With a shared folder, **Remove** and moving a project now correctly forget the old
  location in the shared project list.
- The in-app updater now checks the public CALCIFER repository. Installed versions up
  to 0.2.6 need this version installed once with the setup program; later updates
  arrive through **Settings → Check for updates**.

No data format changes from 0.2.6. This is an unsigned personal Windows x64 build.

### Changes in 0.2.6

- Optional shared folder for using CALCIFER on more than one computer, for example a
  NAS. Set `CALCIFER_SHARED_DIR` (such as `Z:\Calcifer-Data`) to keep the reference
  library, the list of registered projects, and the writing profile there. Each
  computer keeps its own search index and rebuilds it from the shared projects when
  CALCIFER starts.
- If CALCIFER is still open on another computer using the same shared folder, you are
  warned before it opens. If the shared folder cannot be reached, CALCIFER explains
  this instead of opening with local copies.
- To set it up, close CALCIFER on every computer, copy the library folder from
  `%LOCALAPPDATA%\Calcifer` into the shared folder, and set the variable on each
  computer, for example `setx CALCIFER_SHARED_DIR Z:\Calcifer-Data`.

Without `CALCIFER_SHARED_DIR`, behavior is unchanged. No data format changes from 0.2.5.
This is an unsigned personal Windows x64 build.

## 0.2.5 — 2026-10-07

First public release: 0.2.5.

- Projects → **Add folder…** no longer opens a pop-up window to name a new project.
  For a folder without CALCIFER metadata, a bar below the project list asks for the
  name; press **Start project** or Enter. Errors from adding a folder show in the
  page's status line.

No data format changes from 0.2.4. This is an unsigned personal Windows x64 build.
