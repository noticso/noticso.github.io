# Bandit Level 3 → Level 4

## Objective

The password is stored in a hidden file inside the `inhere` directory.

## Solution

I entered the target directory:

```bash
cd inhere
```

A standard `ls` command does not show hidden files. In Linux, a filename beginning with `.` is hidden by default.

To display all entries, including hidden files, I used:

```bash
ls -la
```

After identifying the hidden file, I read it with:

```bash
cat .hidden
```

## Password Retrieved

```text
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

## Key Takeaway

Use `ls -la` when you need to inspect hidden files, file permissions, owners, and sizes.
