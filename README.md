# FIX Bible

A single-file browser tool for decoding, validating, and inspecting FIX protocol messages. No install, no server, no data leaves your machine.

**[Download the latest release](dist/FIX-BIBLE-v4.7.0-generic.html)** — open it directly in your browser.

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20me%20a%20coffee-☕-yellow?style=flat-square&logo=buy-me-a-coffee)](https://buymeacoffee.com/jamesholland)

---

## What it does

Paste any FIX message (or a full log block of many messages) and FIX Bible decodes every tag against the FIX 4.4 standard, shows field names, data types, and descriptions sourced from FIXimate, validates required tags, and flags anything unusual.

**Core features:**

- Auto-detects the delimiter (`SOH`, `|`, `;`) and strips extra text around the message
- Multi-message support — parses a full log block and gives each message its own tab, plus an aggregate "All" view
- Decoded Fields panel with tag number, name, value, data type, and description
- Repeating groups detected and displayed separately
- Validation — missing required tags, unknown tags, basic datatype checks
- Find — multi-token search across tag numbers, names, and values (supports `tag=value`, `=value`, or free text)
- Redaction — sensitive tags (password, raw data, etc.) hidden by default
- Export — Copy TSV, Download CSV, Download JSON, Export Bundle ZIP (all messages, per-message FIX/CSV/JSON + manifest)
- LZ4 decompression — load `.lz4` compressed FIX log files directly
- Upload your own FIX XML dictionary to decode proprietary/custom tags alongside standard ones

## Upload your own dictionary

FIX Bible defaults to the public FIX 4.4 standard. To decode venue-specific or custom tags, upload a FIX XML dictionary (standard QuickFIX/FIX Repository format) using the **Upload dictionary** button. Uploaded entries fall back to FIXimate for any standard tags not defined in your file.

## Run locally from source

```bash
git clone https://github.com/james-holland00/fix-bible.git
python3 -m http.server -d web
```

Then open `http://localhost:8000`.

## Releases

Packaged single-file HTML releases are in [`dist/`](dist/). Each release is self-contained and can be opened directly in a browser or shared as a file.

| Version | File |
|---------|------|
| v4.7.0 | [FIX-BIBLE-v4.7.0-generic.html](dist/FIX-BIBLE-v4.7.0-generic.html) |

See [PATCH-NOTES-generic.txt](dist/PATCH-NOTES-generic.txt) for the full changelog.

## Tag definitions

Standard FIX 4.4 tag names, data types, and descriptions are sourced from the [FIXimate](https://fiximate.fixtrading.org/) public dictionary maintained by the FIX Trading Community.

## License

MIT
