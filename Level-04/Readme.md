# Bandit Level 4 → Level 5

## Introduction

Bandit Level 4 builds on the file-handling skills learned in the previous levels.  
This level introduces the use of the `file` command to identify the type of files.

## Challenge Overview

The password for the next level is stored in one of the files inside the `inhere` directory.

Most of the files contain non-readable data, but one file contains human-readable text. The goal is to identify that file and read its contents.

## Approach and Strategy

1. Connect to the Bandit server as `bandit4`.
2. Enter the `inhere` directory.
3. List the available files.
4. Use the `file` command to identify the type of each file.
5. Find the file identified as ASCII text or human-readable text.
6. Read the contents of that file using `cat`.
7. The output gives the password for the next level.

## Commands Used

Connect to the server:

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```


## After Logging In

### 1. Enter the `inhere` Directory

```bash
cd inhere
```

### 2. List the Files

```bash
ls
```

### 3. Check the File Types

Use the `file` command to check the type of every file:

```bash
file ./*
```

### 4. Read the Human-Readable File

Identify the file containing ASCII text or human-readable data from the output of `file ./*`, then read it:

```bash
cat ./-file07
```

> **Note:** The exact filename should be taken from the output of the `file ./*` command.

## Notes

* `file` is used to determine the type of a file.
* `./*` represents all files in the current directory.
* Most files in this level contain non-readable data.
* The correct file can be identified by looking for an ASCII text or human-readable file.
* `cat` is used to display the contents of the identified file.
* This level introduced the importance of identifying a file's actual type instead of relying only on its filename or extension.

## Conclusion

Bandit Level 4 introduced the `file` command and demonstrated how it can be used to identify unknown file types.

This level helped strengthen my understanding of Linux file analysis and showed how simple commands can be combined to locate useful information efficiently.
