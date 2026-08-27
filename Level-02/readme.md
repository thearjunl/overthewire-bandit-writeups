# Bandit Level 2 → Level 3

## Introduction

Bandit Level 2 builds on the file-handling concepts learned in the previous level.  
This level introduces how to work with filenames that contain spaces.

## Challenge Overview

The goal of this level is to find the password for the next level.

The password is stored in a file named `--spaces in this filename--`.

Because the filename contains spaces, it must be handled correctly when using Linux commands.

## Approach and Strategy

1. Connect to the Bandit server as `bandit2`.
2. List the files in the home directory.
3. Identify the file containing spaces in its name.
4. Use the correct path to read the file.
5. Use the password obtained to access the next level.

## Commands Used

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```


## After Logging In

First, list all files and directories in the current directory:

```bash
ls -la
```

To read the file with spaces in its name:

```bash
cat ./--spaces in this filename--
```

## Notes

* Linux allows spaces in filenames.
* Spaces can cause problems because the shell normally treats them as separators between arguments.
* Using `./` makes it clear that the complete name refers to a file in the current directory.
* The filename can also be enclosed in quotes when it contains spaces.
* For example:

```bash
cat "./--spaces in this filename--"
```

* This level introduced the importance of handling filenames containing spaces correctly.

## Conclusion

Bandit Level 2 introduced another important Linux file-handling concept: filenames can contain spaces.

Using `./` or quotes allows the shell to correctly interpret the complete filename as a single argument. This level improved my understanding of how Linux handles filenames and command-line arguments.
