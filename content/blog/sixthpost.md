---
title: This is the sixth post, that I've created myself.
description: This is a post on My Blog about Static Site Generators.
date: 2023-08-14
tags:
  - SSG
---

# SSG

Static site generators (SSGs) are engines that use text input files (such as Markdown, reStructuredText, and AsciiDoc) to generate static web pages.
Static Site Builders offer distinct advantages

1. Speed
2. Version control for content
3. Security
4. Less hassle with the server
5. Traffic surges

SSGs typically consist of a template written in HTML with a templating system, such as liquid (Jekyll) or Go template (Hugo). The same structure (typically a Git repository) includes content in a plain-text format such as markdown or reStructuredText. A single file often corresponds to a single web page. The website variable settings are stored in a flat-text configuration file _config.yml (YAML), \_config.toml (TOML) or \_config.json (JSON). Page files typically also start with a YAML, TOML or JSON preamble to define variables such as title, permalink, date, etc. Files with names that begin with an underscore (_) such as \_index.md (as opposed to index.md) are considered templates or archetypes and are thus not rendered as pages themselves.
