# CALCIFER

CALCIFER is a local-first project and research workspace for Windows. It keeps
projects, tasks, notes, references, citations, Word integration, and writing checks
in one desktop app. Your data stays on your machine.

- **Projects and tasks:** project metadata lives as plain YAML in each project's
  `.calcifer` folder, so it stays readable and works with Git.
- **Reference library:** a global library with search, tags, notes, PDF preview,
  CSL JSON import/export, Zotero import, and optional DOI lookup.
- **Citations in Word:** insert and refresh citations and bibliographies in desktop
  Word, rendered locally with Pandoc.
- **Writing checks:** deterministic, offline style checks, with optional local
  LanguageTool grammar checks.

## Download and install

1. Open the [latest release](../../releases/latest) and download
   `Calcifer.Desktop-win-x64-Setup.exe`.
2. Run it. CALCIFER installs for your Windows user only, with no administrator rights
   needed.
3. Later updates come through **Settings → Check for updates**. CALCIFER never
   installs an update unless you choose **Install and restart**.

Each release lists its SHA-256 checksums in `SHA256SUMS`. These builds are **not
code-signed**, so Windows SmartScreen may warn the first time you run the
installer.

## Requirements

- Windows 10 or newer, x64.
- Optional tools:
  - [Pandoc](https://pandoc.org/) to render citations.
  - Microsoft Word (desktop) for the Word citation and writing companion.
  - Git, for read-only repository status on a project.
  - A local LanguageTool server, for grammar checks.

Project, library, and writing features work offline without any of these.

## Your data

CALCIFER stores app data in `%LOCALAPPDATA%\Calcifer` and project data in each
project folder. Installing, updating, or uninstalling the app does not move or
delete either. Back up both before upgrading.

## What changed

See [CHANGELOG.md](CHANGELOG.md). Each version's entry names the version it
replaces and lists what changed.

## Source and license

This repository holds release builds and user documentation only. The source code is
developed privately. No license to the source code is granted.
