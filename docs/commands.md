# Linux Command Reference

A compact reference for commands encountered during the Bandit walkthroughs.

| Command | Purpose | Example |
| --- | --- | --- |
| `ls` | Lists files and directories | `ls -la` |
| `cat` | Displays a file's contents | `cat readme` |
| `file` | Identifies a file's content type | `file ./*` |
| `find` | Searches for files using filters | `find . -type f -size 1033c` |
| `grep` | Searches text for a pattern | `grep "millionth" data.txt` |
| `sort` | Sorts lines of text | `sort data.txt` |
| `uniq -u` | Displays lines that appear once | `sort data.txt \| uniq -u` |
| `strings` | Extracts readable strings from binary data | `strings data.txt` |
| `base64 -d` | Decodes Base64 data | `base64 -d data.txt` |
| `tr` | Translates characters | `tr 'A-Za-z' 'N-ZA-Mn-za-m'` |
| `xxd -r` | Reverses a hexadecimal dump | `xxd -r data.txt data` |
| `ssh` | Connects to a remote system securely | `ssh -p 2220 user@host` |
| `scp` | Copies files securely over SSH | `scp -P 2220 user@host:/path/file .` |
| `nc` | Connects to or listens on network ports | `nc localhost 30000` |
| `openssl s_client` | Connects to a TLS-enabled service | `openssl s_client -connect localhost:30001` |
| `diff` | Compares files line by line | `diff --color=auto old new` |

!!! tip
    When a filename starts with `-`, use `./` before the filename. For example: `cat ./-file07`.
