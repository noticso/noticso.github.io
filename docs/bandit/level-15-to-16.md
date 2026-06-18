# Bandit Level 15 → Level 16

## Objective

Send the current password to local port `30001` through an SSL/TLS encrypted connection.

## Solution

Because the service expects TLS, I used OpenSSL instead of a plain Netcat connection:

```bash
openssl s_client -connect localhost:30001
```

After the secure connection was established, I entered the current password.

For less connection metadata, this variation is convenient:

```bash
openssl s_client -connect localhost:30001 -quiet
```

## Password Retrieved

```text
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```

## Key Takeaway

`openssl s_client` is useful for manually testing encrypted services:

```bash
openssl s_client -connect hostname:port
```
