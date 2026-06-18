# Bandit Level 1 → Level 2

## Objective

The password is stored in a file named `-`.

## Solution

A hyphen is normally interpreted by Linux commands as an option or as standard input. Therefore, this command is not suitable:

```bash
cat -
```

To treat the hyphen as a real filename, I used the relative-path prefix `./`:

```bash
cat ./-
```

## Password Retrieved

```text
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

## Key Takeaway

When a filename begins with a hyphen, prepend `./`:

```bash
./filename
```

This tells the shell that the value is a path instead of a command-line option.
