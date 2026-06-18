# Bandit Level 2 → Level 3

## Objective

The password is stored in a file named:

```text
--spaces in this filename--
```

## Solution

The filename presents two issues: it begins with hyphens and contains spaces.

I used `./` to make the file path explicit and escaped every space with a backslash:

```bash
cat ./--spaces\ in\ this\ filename--
```

## Password Retrieved

```text
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```

## Key Takeaway

Spaces can be escaped with `\`:

```bash
cat file\ with\ spaces
```

Alternatively, quotation marks can be used:

```bash
cat "file with spaces"
```
