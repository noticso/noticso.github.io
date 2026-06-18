# Bandit Level 20 → Level 21

## Objective

The `suconnect` binary connects to a local port. If it receives the correct current password, it returns the next password.

## Solution

I created a Netcat listener on local port `1234` and piped the current password into it:

```bash
echo -n "0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO" | nc -l -p 1234 &
```

The command starts the listener in the background. I then passed the **port number** to the setuid binary:

```bash
./suconnect 1234
```

The binary connected to the local listener, received the password, validated it, and returned the next credential.

## Password Retrieved

```text
EeoULMCra2q0dSkYj561DX7s1CpBuOBt
```

## Important Note

When a command runs in the background, the terminal may display output such as:

```text
[1] 18
```

The number `18` is a job or process identifier. It is **not** the network port. The argument for `suconnect` must remain the port chosen for the listener:

```bash
./suconnect 1234
```

## Key Takeaway

This level demonstrates a basic local client-server interaction. It also reinforces the difference between a port number, a process ID, and a shell job number.
