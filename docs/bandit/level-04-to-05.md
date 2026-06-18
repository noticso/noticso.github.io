# Bandit Level 4 → Level 5

## Objective

The password is stored in the only human-readable file inside the `inhere` directory.

## Solution

After moving into the directory, I used `file` to identify the type of every file:

```bash
cd inhere
file ./*
```

Most files contained binary or unreadable content. One file was identified as ASCII text. Its name began with a hyphen, so I used `./` when reading it:

```bash
cat ./-file07
```

## Password Retrieved

```text
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

## Key Takeaway

The `file` command is useful when extensions are missing or filenames are misleading:

```bash
file filename
```

Use it before manually opening a large set of unknown files.
