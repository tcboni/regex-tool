# Regex Tool

A lightweight web app for working with regular expressions.

**[→ Open Regex Tool](https://tcboni.github.io/regex-tool/)**

## Layout

One pattern field on top, your test text on the left, and an inspector on the right. The test text stays in view whatever the inspector shows, and a splitter between the two panes resizes them (double-click to reset).

### Pattern

The pattern reads like a regex literal: `/pattern/flags`. Click a flag letter (`g i m s u v y`) to turn it on or off. Every capture group gets its own color, and a bracket under the pattern marks each group with its number (and name), stacked by nesting depth. Paste a whole literal such as `/\d+/gi` and the pattern and flags are both set.

Syntax errors are marked with a squiggle at the broken part. Matching runs in a background worker with a time limit, so a pattern that backtracks catastrophically — `(a+)+$` on a long string — stops with a message instead of freezing the page.

### Test string

Matches are highlighted in the text, and each capture group is tinted in its color. Zero-width matches such as `\b` or `^` show as thin markers. Put the cursor in a match to find it in the Matches list.

### Matches

Every match with its position and capture groups. Point at a match to find it in the text, click to select it.

### Replace

A live replacement with the full JavaScript syntax: `$1`, `$<name>`, `$&`, `` $` ``, `$'` and `$$`. Chips insert the tokens for the groups your pattern actually has. In the result, text that came from a group keeps the group's color. **Split** shows what `String.prototype.split()` returns, captured groups included.

### Explain

A plain-English breakdown of the pattern as a tree: groups, alternatives, lookarounds, classes and quantifiers. The descriptions follow the active flags (with `m`, `^` is "start of a line"). Point at a row to see which part of the pattern it describes.

### Code

Ready-to-paste code in **11 languages**: JavaScript, TypeScript, Python, Java, C#, Go, Rust, Ruby, PHP, Perl and Bash. The pattern, flags and your replacement string are translated for each language (for example, named groups become `(?P<name>…)` in Python). Notes warn about features a target can't handle, such as lookbehind in Go's RE2 engine.

### Reference

Every piece of syntax, searchable. Click a row to insert it at the cursor; with text selected, groups and lookarounds wrap the selection. `⌘Z` / `Ctrl+Z` undoes an insertion. Includes a helper that escapes literal text for use in a pattern.

### Library

35 ready-to-use patterns in six groups — web, network and IDs, dates and times, numbers, contact details, text and code. Each loads with sample text that shows what it matches and what it rejects; some also load a replacement (for example, converting ISO dates to US dates). **Undo** in the notification brings back what you had before.

## More

- **Share links** — the link button copies a URL that opens the same pattern, flags, text and replacement.
- **Keyboard** — press `/` to jump to the pattern; arrow keys move between tabs.
- Your work is saved in the browser between visits.
