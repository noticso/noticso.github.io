# Bandit Level 17 → Level 18

## Objective

`passwords.old` and `passwords.new` are nearly identical. The password is the only changed line.

## Solution

I compared the files with `diff`:

```bash
diff --color=auto passwords.old passwords.new
```

The line starting with `>` belongs to `passwords.new`, which contains the next password.

## Password Retrieved

```text
x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
```

## Key Takeaway

`diff` compares files line by line:

```bash
diff file1 file2
```

It is useful for configuration reviews, code changes, logs, backups, and incident analysis.
