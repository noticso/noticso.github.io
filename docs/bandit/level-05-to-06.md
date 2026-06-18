# Bandit Level 5 → Level 6

## Objective

The target file inside `inhere` is:

- Human-readable
- Exactly 1033 bytes
- Not executable

## Solution

I used `find` to search recursively for regular files with the required size:

```bash
cd inhere
find . -type f -size 1033c
```

The `c` suffix means bytes. To make the search more precise, I could also exclude executable files and inspect the matching file type:

```bash
find . -type f -size 1033c ! -executable -exec file {} \;
```

After identifying the readable file, I used `cat` to print the password.

## Password Retrieved

```text
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```

## Key Takeaway

`find` can filter by many file properties, including path, type, size, ownership, and permissions.
