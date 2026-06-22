# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

This is the **GitHub profile README** repo (`chrisOTM/chrisOTM`). Its sole purpose
is `README.md`, which GitHub renders at the top of the user's profile page
(github.com/chrisOTM). There is no application code, build step, test suite, or
linter — the "product" is the rendered Markdown.

## Working on it

- All edits happen in `README.md`. It mixes Markdown with inline HTML
  (`<p align="center">`, shields.io badges) for centered layout GitHub's plain
  Markdown can't express.
- Preview rendering against GitHub Flavored Markdown before considering a change
  done; inline HTML behaves differently than local Markdown previewers.

## Keeping the project list current

The "Featured Projects" section is hand-maintained and drifts from reality. To
reconcile it with the user's actual public repos:

    gh repo list chrisOTM --limit 50 --json name,description,primaryLanguage,isFork,updatedAt

Match each featured entry to a live repo, add notable new ones, and keep the
tech-badge row (Python / TypeScript / QML / Kotlin / …) consistent with the
languages actually represented. Repos with empty descriptions need a
description written before they're worth featuring.
