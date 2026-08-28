# Bandit Level 10 → Level 11

## Introduction

Bandit Level 10 introduces **Base64 decoding**.  
This level demonstrates how encoded data can be converted back into its original readable form.

## Challenge Overview

The password for the next level is stored in the file named `data.txt`.

The contents of the file are encoded using Base64. The goal is to decode the content and obtain the password.

## Approach and Strategy

1. Connect to the Bandit server as `bandit10`.
2. Check the files in the home directory.
3. Read the contents of `data.txt`.
4. Identify that the content is Base64 encoded.
5. Use the `base64` command with the decode option.
6. The decoded output contains the password for the next level.

## Commands Used

```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220
```

## After Logging In

First, list the files in the current directory:

```bash
ls
```

Read the encoded data:

```bash
cat data.txt
```

Decode the Base64 content:

```bash
base64 -d data.txt
```

The command decodes the Base64-encoded content in `data.txt` and displays the decoded result.

## Notes

* **Base64** is an encoding method used to represent binary or text data using a limited set of characters.
* Base64 is **not encryption** because it does not provide security or secrecy.
* `base64` is a Linux command used to encode and decode Base64 data.
* The `-d` option tells the command to decode the input.
* `base64 -d data.txt` reads the encoded content from `data.txt` and displays the decoded result.
* This level introduced the difference between **encoding and encryption**.

## Conclusion

Bandit Level 10 introduced Base64 encoding and decoding.

This level helped me understand how encoded information can be recognized and converted back into readable data using standard Linux command-line tools.
