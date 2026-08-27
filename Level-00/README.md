# Bandit Level 0 → Level 1

## Introduction

Bandit Level 0 is the starting point of the OverTheWire Bandit wargame.  
This level introduces the basics of connecting to a remote Linux system using SSH.

## Challenge Overview

The goal of this level is to connect to the Bandit server using SSH with the provided username, hostname, and port.

After connecting to the server, the password for the next level is stored in a file named `readme`.

## Approach and Strategy

1. Connect to the Bandit server using SSH.
2. Check the files available in the home directory.
3. Locate the `readme` file.
4. Read the contents of the file using the `cat` command.
5. Use the obtained password to access the next level.

## Commands Used

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
After logging in:
```bash
ls
cat readme
```
## Notes

- SSH (Secure Shell) is used to securely connect to a remote system.
- The `-p` option specifies the port used for the SSH connection.
- `ls` is used to list files and directories.
- `cat` is used to display the contents of a file.
- Linux commands are case-sensitive.
- This level introduced the basic workflow of connecting to a remote Linux machine and reading files from the command line.

## Conclusion

Bandit Level 0 provided a basic introduction to SSH and Linux command-line usage. It established the foundation for the upcoming levels, where the challenges gradually become more complex.
