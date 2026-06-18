# Bandit Level 12 → Level 13

## Objective

`data.txt` contains a hexadecimal dump of a file that has been compressed multiple times using different archive formats.

## Solution

I created a temporary workspace so that the repeated extraction steps would not affect other files:

```bash
workdir=$(mktemp -d)
cp data.txt "$workdir"
cd "$workdir"
```

First, I reversed the hexadecimal dump into binary data:

```bash
xxd -r data.txt data
```

I then checked the current file type:

```bash
file data
```

Depending on the output, I used the matching extraction command.

=== "gzip"

    ```bash
    mv data data.gz
    gunzip data.gz
    ```

=== "bzip2"

    ```bash
    mv data data.bz2
    bunzip2 data.bz2
    ```

=== "tar archive"

    ```bash
    mv data data.tar
    tar -xf data.tar
    ```

After each extraction, I repeated:

```bash
ls
file *
```

The final result was an ASCII text file, which I read with `cat`.

## Password Retrieved

```text
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```

## Key Takeaway

When analyzing unknown data, do not guess based on the filename. Use `file` after every transformation and select the correct tool for the format detected.
