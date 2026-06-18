# Bandit Level 10 → Level 11

## Objective

The password is stored in `data.txt`, encoded with Base64.

## Solution

Base64 is an encoding format rather than encryption. I decoded the file with:

```bash
base64 -d data.txt
```

## Password Retrieved

```text
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```

## Key Takeaway

To decode Base64 data:

```bash
base64 -d filename
```

To encode a string:

```bash
echo -n "text" | base64
```
