# Bandit Level 5 → Level 6

## Introduction

Bandit Level 5 introduces the use of the `find` command to search for files based on specific conditions.

This level helps understand how Linux can be used to locate a particular file when there are many files and directories.

## Challenge Overview

The password for the next level is stored somewhere in the `inhere` directory.

The correct file has the following properties:

- Human-readable
- 1033 bytes in size
- Not executable

## Approach and Strategy

1. Connect to the Bandit server as `bandit5`.
2. Enter the `inhere` directory.
3. Use the `find` command to search for files matching the given conditions.
4. Identify the file that is 1033 bytes and not executable.
5. Read the contents of the file using `cat`.
6. Use the password obtained to access the next level.

## Commands Used

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
```

## After Logging In

List the contents of the current directory and enter the `inhere` directory:

```bash
ls
cd inhere
```

Search for the required file:

```bash
find . -type f -size 1033c ! -executable
```

Read the identified file:

```bash
cat ./maybehere07/.file2
```

> **Note:** The exact filename may be different depending on the Bandit environment. Use the output of the `find` command to identify the correct file.

## Notes

* `find` is used to search for files and directories.
* `-type f` searches only for regular files.
* `-size 1033c` searches for files with exactly 1033 bytes.
* `! -executable` excludes executable files.
* `cat` is used to display the contents of the identified file.
* Combining multiple conditions with `find` makes it possible to locate a specific file efficiently.
* This level introduced searching for files based on their properties rather than their names.

## Conclusion

Bandit Level 5 introduced the `find` command and showed how different conditions can be combined to locate a specific file.

This level improved my understanding of Linux file searching and demonstrated how command-line tools can make it easier to find information in directories containing many files.
