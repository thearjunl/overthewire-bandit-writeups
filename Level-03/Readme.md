# Bandit Level 3 → Level 4

## Introduction

Bandit Level 3 introduces the concept of **hidden files** in Linux.

This level builds on the file-handling skills learned in the previous levels and shows how files that are not normally displayed can still be accessed from the command line.

## Challenge Overview

The goal of this level is to find the password for the next level.

The password is stored in a hidden file inside the `inhere` directory.

## Approach and Strategy

1. Connect to the Bandit server as `bandit3`.
2. List the files and directories in the home directory.
3. Enter the `inhere` directory.
4. List all files, including hidden files.
5. Identify the hidden file containing the password.
6. Read the file using `cat`.

## Commands Used

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```


## After Logging In

First, list all files and directories in the current directory:

```bash
ls -la
```

Enter the `inhere` directory:

```bash
cd inhere
```

List all files, including hidden files:

```bash
ls -la
```

Read the hidden file:

```bash
cat ...Hiding-From-You

```

## Notes

* Files beginning with `.` are treated as hidden files in Linux.
* `ls` normally does not display hidden files.
* `ls -la` displays all files, including hidden files, with detailed information.
* `cd` is used to change the current directory.
* Hidden files can be accessed normally if their filename is known.
* This level introduced the importance of checking for hidden files when investigating a Linux directory.

## Conclusion

Bandit Level 3 introduced the concept of hidden files in Linux.

Using `ls -la` makes it possible to discover files that are not shown by a normal `ls` command. This level improved my understanding of Linux directory navigation and file discovery.
