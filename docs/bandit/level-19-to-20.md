# Bandit Level 19 → Level 20

## Objective

The next password is stored in `/etc/bandit_pass/bandit20`, but the current user cannot read it directly. A setuid binary named `bandit20-do` is available in the home directory.

## Solution

The binary runs a command with the privileges of user `bandit20`. I used it to read the protected password file:

```bash
./bandit20-do cat /etc/bandit_pass/bandit20
```

## Password Retrieved

```text
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
```

## Key Takeaway

A setuid executable can run with the permissions of its owner rather than the user launching it. This is useful for carefully controlled tasks but can be dangerous when a privileged program is poorly designed.
