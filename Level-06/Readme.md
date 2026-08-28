# Bandit Level 6 → Level 7

## Introduction

Bandit Level 6 builds on the file-searching skills learned in the previous level.  
This level introduces searching the entire Linux filesystem using specific file ownership and size conditions.

## Challenge Overview

The password for the next level is stored somewhere on the server.

The required file has these properties:

- Owned by user `bandit7`
- Owned by group `bandit6`
- Exactly 33 bytes in size

## Approach and Strategy

1. Connect to the Bandit server as `bandit6`.
2. Search the entire filesystem using the `find` command.
3. Filter the results based on:
   - File type
   - Owner
   - Group
   - File size
4. Redirect permission-denied messages so the output is easier to read.
5. Identify the correct file.
6. Read the file using `cat` to obtain the password.

## Commands Used

```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
```

## Search the Entire Filesystem

Use the `find` command to search the entire filesystem:

```bash
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

Read the identified file:

```bash
cat /var/lib/dpkg/info/bandit7.password
```

## Notes

* `find /` searches from the root directory and therefore searches the entire filesystem.
* `-type f` searches only for regular files.
* `-user bandit7` searches for files owned by the `bandit7` user.
* `-group bandit6` searches for files belonging to the `bandit6` group.
* `-size 33c` searches for files that are exactly 33 bytes.
* `2>/dev/null` hides permission-denied error messages.
* Combining multiple conditions makes the search more precise.
* This level introduced the importance of file ownership and permissions when investigating a Linux system.

## Conclusion

Bandit Level 6 introduced a more advanced use of the `find` command by searching the entire filesystem using multiple conditions.

This level helped me understand how file ownership, groups, permissions, and file size can be used together to locate specific files efficiently.
