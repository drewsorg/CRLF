# CRLF
Line ending shenanigans

## Structure

This repository contains two folders with identical sample files, differing only in line ending style:

- **`All LF/`** — all files use Unix-style LF (`\n`) line endings
- **`All CRLF/`** — all files use Windows-style CRLF (`\r\n`) line endings

Each file is exactly **10 lines** with line markers to aid in verifying rendering behavior.

### Files included

| File | Description |
|---|---|
| `.env` | Environment variables config |
| `.gitignore` | Git ignore rules |
| `.dockerignore` | Docker ignore rules |
| `example.json` | JSON package manifest |
| `example.java` | Java class with main method |
| `example.php` | PHP class |
| `example.md` | Markdown document |

## Line ending preservation

A `.gitattributes` file is included at the repository root with `* -text` to **disable Git's automatic line ending normalization**. This ensures that LF and CRLF line endings are committed and checked out exactly as-is, which is critical for this test repository.
