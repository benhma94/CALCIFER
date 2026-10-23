# Changelog

## 0.4.0 — 2026-10-23

Version 0.3.0 → 0.4.0.

- A CALCIFER tab in Word. Choose **Install Word add-in** at the bottom of CALCIFER's
  Word page, then restart Word.
- A quick citation bar: choose **Add/Edit Citation** on the Word tab or press
  Ctrl+Alt+Shift+F11 in Word, type to find references, and press Enter to insert the
  citation at the cursor.
- Settings > Appearance: choose System, Light or Dark, and an accent colour (flame
  orange, blue, green, teal, purple or rose). Changes apply at once and are remembered
  on each computer.
- On a project's Overview, Description and Coauthors are separated by a divider you
  can drag to give either more room.
- On a project's References tab, **Add from library** lists matches as you type
  instead of showing the whole library.

## 0.3.0 — 2026-10-23

Version 0.2.14 → 0.3.0.

- A refreshed look: flatter tables, clearer buttons, and coloured labels for task and
  project status and priority. The app follows the Windows light or dark setting,
  including the title bar.
- The sidebar shows the CALCIFER flame and name at the top. Home opens with counts of
  active projects, open tasks, overdue tasks, and tasks due this week, and overdue
  dates are shown in red.
- Settings has a single heading above its Updates and Workspace tabs.
- On a project's Tasks tab and on the Lists page, **New** sits beside the filters,
  task buttons stay disabled until a task is selected, and Ctrl+Up / Ctrl+Down move
  the selected task.

## 0.2.14 — 2026-10-22

Version 0.2.13 → 0.2.14.

- Project pages no longer show the empty Activity tab.

## 0.2.13 — 2026-10-16

Version 0.2.12 → 0.2.13.

- Faster startup: the window no longer waits for a full reference-library scan, and the
  Library page reads reference files in parallel.
- Only one CALCIFER window runs per data folder; launching again brings the open
  window to the front.
- Project and list task views share a filter bar: filter by title, category, and
  status, and sort tasks.
- The home page's open-task count includes tasks from non-archived lists.

## 0.2.12 — 2026-10-11

Version 0.2.11 → 0.2.12.

- Enhance task navigation: implement double-click functionality for tasks and owners, save pending edits, and update UI behavior
- Enhance task editor synchronization: update status handling, improve autosave behavior, and refine UI elements
- Implement task autosave feature and update UI components for clarity

Drafted from commit messages by the publish workflow.

## 0.2.11 — 2026-10-10

Version 0.2.10 → 0.2.11.

- Rename Home's "Upcoming deadlines" to "Outstanding tasks" and include open tasks
  without a due date, listed after dated tasks.
- Add a "Sort by" selector to the Home task table: due date or priority.
- Simplify task statuses to In progress, Deferred, Done, and Cancelled. New and
  reopened tasks start as In progress. Existing Backlog and Next tasks load as In
  progress and Blocked tasks as Deferred; files are updated on the next save.
- Suggest stages that match the project's type; changing the type refreshes the
  list, and a saved stage that is not in the list is kept.
- Task tables: remove the Order column (Move up/down remain) and rename "Note" to
  "Linked note".

## 0.2.10 — 2026-10-09

Version 0.2.9 → 0.2.10.

- Add general to-do lists for tasks that belong to no project (administration,
  teaching, personal). A new Lists page after Projects creates, renames, archives, and
  restores lists and edits their tasks. Lists are stored in the shared data folder, so
  they appear on every computer that shares it.
- Show list task deadlines alongside project deadlines on Home; double-click a row to
  open its list.
- Show general lists under a "Lists" heading on the phone task page, editable the same
  way as project tasks.

## 0.2.9 — 2026-10-09

Version 0.2.8 → 0.2.9.

- Add coauthor management features: merge details across projects and suggest previous coauthors
- Optimize project opening speed by reusing ProjectDetailView and enhancing task editor initialization
- Update project name and description across documentation and code

Drafted from commit messages by the publish workflow.

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
