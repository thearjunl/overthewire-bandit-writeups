# Bandit Level 14 → Level 15

## Introduction

Bandit Level 14 introduces basic network communication using a local TCP service.

The objective is to submit the current level password to a service running on `localhost` at port `30000` and retrieve the password for the next level.

## Challenge Overview

The password for the next level can be retrieved by submitting the password of the current level to port `30000` on `localhost`.

The `nc` (Netcat) command can be used to communicate with the service.

## Approach and Strategy

1. Log in to the Bandit server as `bandit14`.
2. Identify the current level password.
3. Connect to the service running on `localhost` port `30000` using Netcat.
4. Submit the Bandit Level 14 password to the service.
5. Verify the response from the service.
6. Save the returned password for use in Level 15.

## Commands Used

### Connect to the local service

```bash
nc localhost 30000
```


## Submit the Current Password

After connecting to the service running on `localhost` port `30000`, enter the Bandit Level 14 password.

```bash
nc localhost 30000
```

Then submit the current password:

```text
<Bandit Level 14 password>
```

If the password is correct, the service responds with:

```text
Correct!
```

The service then provides the password required for the next level.

## Notes

* `nc` stands for **Netcat** and is commonly used for network communication.
* `localhost` refers to the local machine.
* Port `30000` is the TCP port where the required service is running.
* Netcat can be used to connect to TCP and UDP services.
* The service verifies whether the submitted password is correct.
* A successful response confirms that the password was accepted.
* This level introduced the concept of interacting with a network service through a specific TCP port.

## Conclusion

Bandit Level 14 introduced basic TCP communication using **Netcat**.

By connecting to the local service on port `30000` and submitting the current password, I was able to retrieve the password required for **Level 15**.

