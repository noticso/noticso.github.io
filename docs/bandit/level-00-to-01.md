# Bandit Level 0 → Level 1

## Objective

The password for the next level is stored in a file named `readme` in the current directory.

## Solution

I started by listing the files available in the directory:

```bash
ls
```

The output showed a file named `readme`. Since it was a normal text file, I displayed its contents with:

```bash
cat readme
```

## Password Retrieved

```text
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```

## Key Takeaway

- `ls` lists files and directories.
- `cat` displays the contents of a text file.

Before using complex commands, enumerate the current directory and inspect the files already available.
