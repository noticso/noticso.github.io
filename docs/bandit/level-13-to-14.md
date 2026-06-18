# Bandit Level 13 → Level 14

## Objective

This level provides a private SSH key instead of the next password. The key must be copied locally and used to log in as `bandit14`.

## Solution

From my local machine, I copied the key with Secure Copy Protocol (SCP):

```bash
scp -P 2220 bandit13@bandit.labs.overthewire.org:/home/bandit13/sshkey.private .
```

I restricted the key permissions so that only my user could read it:

```bash
chmod 600 sshkey.private
```

Then I connected using the private key:

```bash
ssh -i sshkey.private -p 2220 bandit14@bandit.labs.overthewire.org
```

After logging in, I read the password file:

```bash
cat /etc/bandit_pass/bandit14
```

## Password Retrieved

```text
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```

## Key Takeaway

SSH key authentication is commonly used for secure remote administration. Private keys must be protected, which is why `chmod 600` is required.
