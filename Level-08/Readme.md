# Bandit Level 8 → Level 9

## Introduction

Bandit Level 8 introduces the use of `sort` and `uniq` to analyze repeated lines in a text file.

This level helps understand how Linux commands can be combined together to filter and identify unique information.

## Challenge Overview

The password for the next level is stored in the file named `data.txt`.

The password is the only line that occurs exactly once in the file.

## Approach and Strategy

1. Connect to the Bandit server as `bandit8`.
2. Check the files in the home directory.
3. Identify the `data.txt` file.
4. Sort the contents of the file so that identical lines are placed together.
5. Use `uniq` to identify the line that occurs only once.
6. The unique line is the password for the next level.

## Commands Used

```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
```
## After Logging In

First, list the files in the current directory:

```bash
ls
```

Sort the contents and find the unique line:

```bash
sort data.txt | uniq -u
```

The command sorts the contents of `data.txt` and displays the line that occurs only once.

## Notes

* `sort` arranges lines of text in alphabetical or numerical order.
* `uniq` is used to detect or remove repeated lines.
* The `-u` option with `uniq` displays only lines that occur exactly once.
* `sort` is used before `uniq` because `uniq` checks only adjacent duplicate lines.
* The `|` symbol is called a **pipe** and passes the output of one command to another command.
* This level introduced the idea of combining multiple Linux commands to solve a problem efficiently.

## Conclusion

Bandit Level 8 introduced `sort`, `uniq`, and the Linux pipe operator.

This level demonstrated how simple commands can be combined together to analyze large amounts of text and identify specific information efficiently.
