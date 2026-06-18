# Bandit Level 16 → Level 17

## Objective

The next credential is available through a TLS-enabled service running on a port between `31000` and `32000`.

## Solution

I scanned the range and asked Nmap to identify service versions:

```bash
nmap -sV -p 31000-32000 localhost
```

The scan showed two SSL-related services. One was an echo service; the other, on port `31790`, was the target.

I connected using OpenSSL and kept the input stream open:

```bash
openssl s_client -ign_eof -connect localhost:31790
```

After sending the current password, the service returned an RSA private key. This key is the credential for the next level.

I saved it locally, restricted its permissions, and used it to log in:

```bash
chmod 600 sshkey.private
ssh -i sshkey.private -p 2220 bandit17@bandit.labs.overthewire.org
```

## Key Takeaway

A port being open does not prove it is the correct target. Service discovery and protocol identification are necessary before choosing the right connection tool.
