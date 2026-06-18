# Bandit Level 14 → Level 15

## Objective

Send the current password to the service listening on local port `30000`.

## Solution

The service runs on `localhost`, meaning it is reachable from the Bandit machine itself. I connected directly with Netcat:

```bash
nc localhost 30000
```

I then entered the password from the previous level. The server validated it and returned the password for the next user.

A non-interactive version is:

```bash
printf '%s\n' 'MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS' | nc localhost 30000
```

## Password Retrieved

```text
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```

## Key Takeaway

`localhost` refers to the current system. Netcat can make basic TCP connections with this syntax:

```bash
nc hostname port
```
