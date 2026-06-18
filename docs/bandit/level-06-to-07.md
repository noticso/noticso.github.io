# Bandit Level 6 → Level 7

## Objective

The password is stored somewhere on the server in a file that is:

- Owned by user `bandit7`
- Owned by group `bandit6`
- Exactly 33 bytes in size

## Solution

Because the file could be located anywhere, I searched from the root directory:

```bash
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

The command searches only for regular files and filters them by user, group, and exact size. The `2>/dev/null` redirection suppresses permission-denied messages.

Once I found the path, I used `cat` to read the file.

## Password Retrieved

```text
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```

## Key Takeaway

Error redirection is particularly helpful during system-wide searches:

```bash
2>/dev/null
```

It hides error output while preserving the useful results.
