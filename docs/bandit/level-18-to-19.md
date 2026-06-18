# Bandit Level 18 → Level 19

## Objective

The password is stored in `readme`, but the account's `.bashrc` file logs the user out immediately during a normal interactive SSH session.

## Solution

Instead of opening an interactive session, I executed the command directly through SSH:

```bash
ssh -p 2220 bandit18@bandit.labs.overthewire.org "cat readme"
```

This bypasses the modified interactive shell behavior and returns the file contents.

Another option is to invoke a different shell:

```bash
ssh -p 2220 -t bandit18@bandit.labs.overthewire.org /bin/sh
```

## Password Retrieved

```text
cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
```

## Key Takeaway

SSH can execute one remote command without opening an interactive terminal:

```bash
ssh user@host "command"
```
