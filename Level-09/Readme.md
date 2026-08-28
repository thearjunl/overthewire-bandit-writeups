# Bandit Level 9 → Level 10

## Introduction

Bandit Level 9 introduces the use of the `strings` command to extract readable text from binary files.

This level helps understand how useful information can sometimes be hidden inside files that are not meant to be read directly as normal text.

## Challenge Overview

The password for the next level is stored in the file named `data.txt`.

The file contains mostly binary data, but the password is stored as one of the human-readable strings.

## Approach and Strategy

1. Connect to the Bandit server as `bandit9`.
2. Check the files in the home directory.
3. Identify the `data.txt` file.
4. Use the `strings` command to extract readable text from the file.
5. Search through the output for the required password.
6. Use the discovered password to access the next level.

## Commands Used

```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
```

## After Logging In

First, list the files in the current directory:

```bash
ls
```

Extract readable strings from the file:

```bash
strings data.txt
```

To make the search easier, `grep` can also be combined with `strings`:

```bash
strings data.txt | grep "="
```

The command extracts readable strings from `data.txt` and filters the output to show lines containing `=`.

## Notes

* `strings` extracts sequences of printable characters from binary files.
* Binary files may contain readable text mixed with non-readable data.
* `grep` can be used to filter the output and find specific patterns.
* The `|` (pipe) operator sends the output of one command to another command.
* Combining commands can make searching through large amounts of data more efficient.
* This level introduced the idea of extracting useful information from binary data instead of treating the entire file as normal text.

## Conclusion

Bandit Level 9 introduced the `strings` command and demonstrated how readable information can be extracted from binary files.

This level improved my understanding of how to investigate files that contain both binary and human-readable data using Linux command-line tools.
