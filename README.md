# Regex Tool

A lightweight web app for working with regular expressions.

**[→ Open Regex Tool](https://tcboni.github.io/regex-tool/)**

## Features

The tool is organized into seven tabs, all sharing one pattern + flags input at the top.

### Tester

Live highlighting of every match as you type. Hover a match in the side panel and the corresponding highlight pulses in the test string. Each match shows its index range, full text, numbered capture groups, and named capture groups.

### Replace

Run a replacement against the test string and see the result instantly. Supports the full JavaScript replacement syntax: `$1` / `$2` for numbered groups, `$<name>` for named groups, `$&` for the full match, `` $` `` and `$'` for the text before / after the match. A Split panel below shows how the regex splits the input.

### Explain

Walks the pattern character by character and prints a tagged, indented English description of every token — literals, character classes, quantifiers (greedy / lazy / possessive), anchors, groups (capturing, non-capturing, named, lookahead, lookbehind in all four polarities), backreferences, unicode escapes, and more.

### Builder

Click chips to append regex fragments at the cursor: character classes, anchors, quantifiers, groups, lookarounds, special characters. Includes a "escape a literal string" helper that turns raw text into a regex-safe pattern.

### Library

30+ ready-to-use patterns: email, URL, IPv4 / IPv6, US and international phone numbers, multiple date formats, ISO timestamps, UUIDs, hex colors, slugs, usernames, strong passwords, credit cards, postal codes (US / UK), integers / decimals / scientific notation, HTML tags, Markdown links, whitespace lines, duplicate words, JWTs, MAC addresses, semantic versions, Twitter handles, hashtags, and more. Clicking a pattern loads it **with a relevant sample test string** so you can immediately see it in action.

### Cheatsheet

A compact reference for character classes, anchors, quantifiers, groups, lookaround, flags, escape sequences, and replacement specials.

### Code

Generates ready-to-paste code in **11 languages** from your current regex + flags: JavaScript, TypeScript, Python, Java, C#, Go, Rust, Ruby, PHP, Perl, and Bash (grep + sed). Flag translations are handled per language.
