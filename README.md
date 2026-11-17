# tuile

**One place for all your work, and every agent doing it.**

tuile is a desktop app for planning projects, writing docs and answering your agents' questions.
Hand a task to Claude Code, Codex or any model through [Pi](https://github.com/badlogic/pi-mono), and switch whenever you like.
Your tasks and pages stay on your Mac.

This repository holds the official downloads and the public issue tracker.
The product source is private.

## Download for Mac

1. Download the newest `tuile-<version>-macos-arm64.dmg` from [the latest release](https://github.com/tuilehq/releases/releases/latest).
2. Open it and drag **Tuile** to Applications.
3. Open Tuile from Applications.

tuile needs a Mac with Apple silicon and macOS 13 or later.
The app is signed and notarized.
It checks for a new version every four hours and installs it when you click **Update ready** or next quit.

There is no download for Intel Macs, Linux or Windows yet.

## Use it from Claude Code

The tuile plugin gives Claude Code your tasks and work order, with `/tuile:capture`, `/tuile:next` and `/tuile:handoff`.
Install tuile first, then in Claude Code:

```
/plugin marketplace add tuilehq/releases
/plugin install tuile@tuile
```

Run `/tuile:setup` to check it can reach tuile.
The plugin lives in [claude-plugin](claude-plugin).

## The first run

1. At **What do you want to work on today?**, use the folder button to choose a folder or create a project.
2. Type your first request and press Enter, or click **Skip for now** to look around.
3. Sign in with the AI provider you already use or enter an API key, then click **Continue**.
   You can also skip sign-in and connect an AI later.

Once you’ve connected an AI, add a task, select it and press `a` to hand it to an agent.
When the agent has a question or a result to review, it lands in the Inbox.

The [user guide](https://tuile.dev/docs/) covers the rest, starting with [Get started](https://tuile.dev/docs/get-started/).

## What you need

tuile has no account of its own and no hosted task service.
It uses the AI subscription or API key you already have.

| For | Install |
| --- | --- |
| The Git page and pull requests | The [GitHub CLI](https://cli.github.com/), then run `gh auth login` |
| Claude Code or Codex as your agent | The agent itself, signed in as usual |

## Alpha status

tuile is an alpha, used every day by its author.
Expect rough edges, and back up your tasks before you rely on it:

```sh
tuile storage backup --file ~/Backups/tuile.sqlite3
```

Tasks and settings live in `~/.tuile`.
[Your data](https://tuile.dev/docs/your-data/) lists what is stored, where, and what leaves your computer.

## Report a problem

[Open an issue](https://github.com/tuilehq/releases/issues) with the output of `tuile build-id`, what you did and what happened.
If you attach a log folder, read it first: it can name your tasks and folders.
[Troubleshooting](https://tuile.dev/docs/troubleshooting/) shows where the logs are.

## The terminal app

tuile was called Switchbard, and its command `sbt`, until November 2026.
The terminal releases through **v0.4.0-alpha.4** have been withdrawn.
The Mac app now brings the `tuile` command with it, and there is no separate terminal download yet.

## Licensing

Official builds are free to download and use, for personal or commercial work, on any number of your own devices, under [LICENSE-OFFICIAL-BUILDS](LICENSE-OFFICIAL-BUILDS).
They may not be redistributed, modified or resold.
The product source is private and is not licensed.

The withdrawn releases, through **v0.4.0-alpha.4**, were published under MIT.
The [historical MIT notice](LICENSE-MIT) remains available for existing copies.

The documentation in this repository has the separate limited permissions in [LICENSE](LICENSE).
The Claude Code plugin in [claude-plugin](claude-plugin) is MIT licensed under [its own LICENSE](claude-plugin/LICENSE); the app it connects to is not.
The "Source code" archives GitHub adds to every release hold only this page and the licenses, never tuile's source.
