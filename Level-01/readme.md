# Bandit Level 1 → Level 2

## Introduction

Bandit Level 1 builds on the basic Linux skills learned in Level 0.  
This level introduces how to work with files that have unusual names.

## Challenge Overview

The goal of this level is to find the password for the next level.  
The password is stored in a file named `-` in the home directory.

Since `-` is commonly interpreted by Linux commands as standard input or an option, it needs to be handled carefully.

## Approach and Strategy

1. Connect to the Bandit server as `bandit1`.
2. List the files in the home directory.
3. Identify the file named `-`.
4. Use `cat` with the correct path to read the file.
5. Use the password obtained to access the next level.

## Commands Used

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

## After Logging In

First, list all files and directories in the current directory:

```bash
ls -la
```

To read the file named `-`, use:

```bash
cat ./-
```

## Notes

* A filename beginning with `-` can be interpreted as an option by many Linux commands.
* Using `./` tells Linux that `-` is a filename in the current directory.
* `cat ./-` reads the contents of the file named `-`.
* `ls -la` displays all files, including hidden files, along with detailed information.
* This level introduced the importance of handling filenames carefully when working with Linux commands.

## Conclusion

Bandit Level 1 introduced an important Linux concept: filenames can sometimes conflict with command options.

Using `./` allows the file to be referenced explicitly and safely. This level helped strengthen my understanding of Linux file handling and command-line behavior.
