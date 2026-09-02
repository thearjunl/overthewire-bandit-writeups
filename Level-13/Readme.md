# Bandit Level 13 → Level 14

## Introduction

Bandit Level 13 introduces SSH private keys and shows how they can be used to authenticate to a remote Linux system without using a password.

## Challenge Overview

The goal of this level is to use the private SSH key provided in the home directory to log in to the `bandit14` user.

The private key is stored in a file named:

```text
sshkey.private
```


## Approach and Strategy

1. Log in to the Bandit server as `bandit13`.
2. List the files in the home directory.
3. Identify the `sshkey.private` file.
4. Display and copy the private SSH key to the local Kali machine.
5. Save the key as `bandit14_pvk_ssh.key`.
6. Set the correct permissions on the private key.
7. Use the private key with SSH to log in as `bandit14`.

## Commands Used

### 1. List the Files

```bash
ls
```

### 2. Display Detailed Information

```bash
ls -la
```

### 3. Read the Private SSH Key

```bash
cat sshkey.private
```

Copy the displayed private key to the local Kali machine and save it as:

```text
bandit14_pvk_ssh.key
```

### 4. Set the Correct Permissions

On the Kali machine:

```bash
sudo chmod 600 bandit14_pvk_ssh.key
```

### 5. Connect to `bandit14` Using the Private Key

```bash
ssh bandit14@bandit.labs.overthewire.org -p 2220 -i bandit14_pvk_ssh.key
```

## Important Note

The `bandit14_pvk_ssh.key` file was kept in the **same parent folder as the `Bandit` repository/folder** so that it could be easily accessed when connecting to the next level.

Example directory structure:

```text
Desktop/
├── Bandit/
│   ├── Level-00/
│   ├── Level-01/
│   ├── Level-02/
│   ├── ...
│   └── Level-13/
│
└── bandit14_pvk_ssh.key
```

> **Security Warning:** The private SSH key should **never be uploaded to GitHub** because it is sensitive authentication information.

## Notes

* SSH can authenticate users using private keys instead of passwords.
* The `-i` option specifies the private key that SSH should use.
* Private SSH keys require appropriate file permissions.
* `chmod 600` restricts the key so that only the owner can read and write it.
* `ls -la` is useful for finding hidden files and checking file permissions.
* The `cat` command can be used to display the contents of a file.
* Private keys should never be committed to a public GitHub repository.
* This level introduced **SSH key-based authentication**.

## Conclusion

Bandit Level 13 introduced SSH private-key authentication.

I found the `sshkey.private` file, copied the private key to my Kali machine, changed its permissions using `chmod 600`, and used the key with SSH to successfully log in as `bandit14`.

The key lesson from this level was understanding how **SSH private keys can be used for authentication** and why protecting private key files is essential.
