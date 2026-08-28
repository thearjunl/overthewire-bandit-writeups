# Bandit Level 12 → Level 13

## Introduction

Bandit Level 12 introduces working with **hexadecimal dumps, compression, and archive files**.

This level is more challenging because the file is compressed multiple times using different formats. It requires identifying each format and processing it step by step.

## Challenge Overview

The password for the next level is stored in `data.txt`.

However, the file is a **hexadecimal dump** of a file that has been repeatedly compressed.

The goal is to convert the hexadecimal dump back into its original binary form and then decompress or extract each layer until the password is revealed.

## Approach and Strategy

1. Connect to the Bandit server as `bandit12`.
2. Create a temporary working directory.
3. Copy `data.txt` into the working directory.
4. Convert the hexadecimal dump back into binary data using `xxd`.
5. Use the `file` command to identify the file format.
6. Rename the file when necessary so the appropriate decompression tool can recognize it.
7. Decompress or extract the file.
8. Run `file` again on the resulting file.
9. Repeat the process until the final file contains readable text.
10. Read the final file to obtain the password for the next level.

## Commands Used

Connect to the server:

```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220
```

## After Logging In

### 1. Create a Temporary Working Directory

Create a temporary directory and move into it:

```bash
mkdir /tmp/bandit12
cd /tmp/bandit12
```

### 2. Copy the File

Copy `data.txt` into the temporary working directory:

```bash
cp ~/data.txt .
```

### 3. Convert the Hexadecimal Dump Back into Binary

Use `xxd -r` to convert the hexadecimal dump back into binary data:

```bash
xxd -r data.txt data
```

### 4. Identify the File Type

Use the `file` command to determine what type of file you have:

```bash
file data
```

### 5. Extract Gzip Compressed Files

If the file is identified as gzip-compressed:

```bash
mv data data.gz
gunzip data.gz
```

### 6. Extract Bzip2 Compressed Files

If the file is identified as bzip2-compressed:

```bash
mv data data.bz2
bunzip2 data.bz2
```

### 7. Extract Tar Archives

If the file is identified as a tar archive:

```bash
tar -xf data
```

### 8. Identify the File After Each Extraction

After every extraction or decompression, check the resulting file:

```bash
file <filename>
```

Repeat the appropriate extraction or decompression process until the actual data is reached.

### 9. Read the Final Text File

When the file is finally identified as ASCII text, display its contents:

```bash
cat <filename>
```

## Notes

* `xxd -r` converts a hexadecimal dump back into binary data.
* `file` is useful for identifying unknown file formats.
* `gzip` compression can be handled using `gunzip`.
* `bzip2` compression can be handled using `bunzip2`.
* `tar` is commonly used to create and extract archives.
* A file can contain multiple layers of compression and archives.
* The file extension does not always tell us what type of file it is, so using `file` is a better way to identify it.
* Creating a temporary directory is useful when working with files that need to be repeatedly modified or extracted.
* This level demonstrated the importance of investigating a file before deciding which tool to use.

## Conclusion

Bandit Level 12 introduced a more advanced approach to file analysis by combining hexadecimal conversion, compression, and archive extraction.

The main lesson was to **identify the file type first, use the appropriate tool, and repeat the process until the actual data is reached**.

This level improved my understanding of Linux file analysis and taught me how to approach multi-layered data systematically.
