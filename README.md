# Scribe

A desktop writing app for fiction, scientific reports, email and presentations. It reads
what you write and points at what could be clearer, on your own machine, with no account
and no model. AI help is optional and uses a model you run yourself.

This repository holds Scribe's installers and release notes. The source is not public.

## Download

Get the newest version from
**[the latest release](https://github.com/pylvir-labs/scribe-releases/releases/latest)** and
pick the file for your system:

| Your system | File |
|---|---|
| Windows 10 or 11 | `Scribe_<version>_x64-setup.exe` |
| macOS, Apple Silicon | `Scribe_<version>_aarch64.dmg` |
| macOS, Intel | `Scribe_<version>_x64.dmg` |
| Linux, Debian or Ubuntu | `Scribe_<version>_amd64.deb` |
| Linux, Fedora or openSUSE | `Scribe-<version>-1.x86_64.rpm` |
| Linux, anything else | `Scribe_<version>_amd64.AppImage` |

The `.msi` is the same Windows app, for those who deploy with Windows Installer. The two
`.app.tar.gz` files are the macOS app without its disk image, and you do not need them.

**Version 0.6.0 has its Windows installers only, for now.** Its Linux and macOS files are added
to the same release in November. Until then, on Linux or macOS, take
[0.5.1](https://github.com/pylvir-labs/scribe-releases/releases/tag/v0.5.1).

## The first launch

The installers are not signed, so your system warns you the first time. That is expected.

- **Windows:** on the SmartScreen notice, choose *More info*, then *Run anyway*.
- **macOS:** right-click the app and choose *Open*, then confirm. Or, in a terminal:
  `xattr -dr com.apple.quarantine /Applications/Scribe.app`
- **Linux:** for the AppImage, `chmod +x Scribe_*.AppImage` and run it. The `.deb` and the
  `.rpm` install like any other package.

## How well each system is tested

| System | Status |
|---|---|
| Windows | Installed and used by the author for every release |
| Linux | Built for every release. The `.deb` has been installed and started under Ubuntu on WSL2, and has had far less use than the Windows build |
| macOS | Built for every release and **never run on a Mac**. If it does not start for you, please say so |

## Updating

To update, download the installer of the newer version and run it. Your documents stay
where you saved them: Scribe keeps no copies of its own.

Since version 0.6.0, Scribe tells you when a newer version is out, under
*Settings ▸ Updates*, and opens this page for you. It never downloads or installs anything by
itself. Checking automatically is off until you turn it on, and a check sends the app's name
and version and nothing about you or your writing.

Version 0.5.1 and earlier do not check: install 0.6.0 by hand once, and it tells you after that.

## What it needs

- **Windows:** the WebView2 runtime, which Windows 10 and 11 have with Edge.
- **Nothing else to write.** The analysis and its findings, grammar and spelling, PDF export,
  slides and diagrams run on your machine with no network. The thesaurus downloads its word
  list the first time you look a word up, and works offline after that.
- **Optional, for the AI features:** [Ollama](https://ollama.com) running on your machine.

## Problems

Open an issue in this repository, and say which system you are on and which version you
installed.
