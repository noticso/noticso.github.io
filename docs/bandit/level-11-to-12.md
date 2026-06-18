# Bandit Level 11 → Level 12

## Objective

The password in `data.txt` was encoded with ROT13, a simple Caesar cipher that rotates letters by 13 positions.

## Solution

I used `tr` to map every uppercase and lowercase letter to its ROT13 equivalent:

```bash
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
```

## Password Retrieved

```text
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```

## Key Takeaway

ROT13 is reversible: applying the same transformation twice returns the original text. It is useful as an encoding exercise but is not secure encryption.
