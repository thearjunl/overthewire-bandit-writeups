# Bandit Level 7 → Level 8

## Introduction

Bandit Level 7 introduces the use of `grep` to search for specific text inside a file.

This level helps understand how to efficiently find required information when a file contains a large amount of text.

## Challenge Overview

The password for the next level is stored in the file named `data.txt`.

The password is located on the same line as the word `millionth`.

## Approach and Strategy

1. Connect to the Bandit server as `bandit7`.
2. Check the files in the home directory.
3. Identify the `data.txt` file.
4. Use `grep` to search for the keyword `millionth`.
5. Read the matching line to obtain the password for the next level.

## Commands Used

```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
```

## After Logging In

First, list the files in the current directory:

```bash
ls
```

Search for the required word:

```bash
grep "millionth" data.txt
```

The command returns the line containing `millionth` along with the password.

## Notes

* `grep` is used to search for specific text or patterns inside files.
* `grep "millionth" data.txt` searches for the word `millionth` in `data.txt`.
* `grep` is especially useful when working with large files where manually searching would be inefficient.
* Quotation marks are used around the search term to clearly define the text being searched.
* This level introduced a simple but powerful method for filtering information from text files.

## Conclusion

Bandit Level 7 introduced the `grep` command and demonstrated how it can be used to quickly find specific information inside a large text file.

This level improved my understanding of searching and filtering information from text files using Linux command-line tools.
