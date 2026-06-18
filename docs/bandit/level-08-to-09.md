# Bandit Level 8 → Level 9

## Objective

The password is the only line in `data.txt` that appears exactly once.

## Solution

`uniq -u` prints lines that appear once, but duplicate lines must first be adjacent. I therefore sorted the file before using `uniq`:

```bash
sort data.txt | uniq -u
```

## Password Retrieved

```text
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```

## Key Takeaway

The pipe symbol passes the output of one command to another:

```bash
command1 | command2
```

Here, `sort` groups identical lines together and `uniq -u` selects the unique line.
