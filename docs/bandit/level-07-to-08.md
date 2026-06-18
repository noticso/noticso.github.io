# Bandit Level 7 → Level 8

## Objective

The password is located in `data.txt` next to the word `millionth`.

## Solution

I used `grep` to search for the keyword:

```bash
grep "millionth" data.txt
```

The command returned the matching line and the password.

## Password Retrieved

```text
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```

## Key Takeaway

`grep` searches text for a pattern:

```bash
grep "keyword" filename
```

It is essential for analyzing logs, configuration files, wordlists, and large text files.
