# Bandit Level 9 → Level 10

## Objective

The password is one of the few human-readable strings in `data.txt` and is preceded by several `=` characters.

## Solution

The file contains mostly unreadable data, so I first extracted text strings with `strings` and then filtered the result with `grep`:

```bash
strings data.txt | grep "=="
```

## Password Retrieved

```text
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```

## Key Takeaway

Use `strings` to extract readable sequences from binary or mixed-content files:

```bash
strings filename
```

Then combine it with `grep` to locate a recognizable pattern.
