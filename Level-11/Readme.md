# Bandit Level 11 → Level 12

## Introduction

Bandit Level 11 introduces **ROT13**, a simple substitution cipher where each letter is shifted by 13 positions in the alphabet.

This level helps understand how basic encoded or obfuscated text can be converted back into readable information.

## Challenge Overview

The password for the next level is stored in the file named `data.txt`.

The contents of the file have been encrypted using ROT13. The goal is to decode the text and obtain the password.

## Approach and Strategy

1. Connect to the Bandit server as `bandit11`.
2. Check the files in the home directory.
3. Read the contents of `data.txt`.
4. Identify that the text has been encoded using ROT13.
5. Decode the text by shifting each letter 13 positions.
6. The decoded text contains the password for the next level.

## Commands Used

```bash
ssh bandit11@bandit.labs.overthewire.org -p 2220
```

## After Logging In

First, list the files in the current directory:

```bash
ls
```

Read the encoded content:

```bash
cat data.txt
```

Decode the ROT13 text:

```bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```

The command translates each alphabetic character by 13 positions, converting the ROT13-encoded text back into readable text.

## Notes

* **ROT13** stands for "Rotate by 13 places."
* Each letter is replaced by the letter 13 positions away in the alphabet.
* ROT13 is a simple substitution cipher and does not provide real security.
* The `tr` command is used to translate or replace characters.
* The pipe `|` passes the output of `cat` to the `tr` command.
* Since applying ROT13 twice returns the original text, the same command can be used for encoding and decoding.
* This level introduced the concept of simple substitution ciphers and character transformation in Linux.

## Conclusion

Bandit Level 11 introduced ROT13 and the `tr` command for character substitution.

This level helped me understand how simple ciphers work and how Linux commands can be combined to decode information directly from the terminal.
