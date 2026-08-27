# OverTheWire Bandit – Linux & Cybersecurity Learning

This repository documents my learning journey through the **Bandit wargame** from [OverTheWire](https://overthewire.org/wargames/).

## Introduction

OverTheWire is a collection of security-related wargames designed to help learners improve their Linux, networking, programming, and cybersecurity skills through practical challenges.

I am currently working through the **Bandit** wargame, which is mainly focused on learning the Linux command line and developing problem-solving skills.

Instead of only solving the challenges, I am documenting the commands, approaches, and concepts I learn from each level.

## Challenge Overview

The Bandit wargame consists of a series of levels where each level provides a challenge that must be solved to obtain the password for the next level.

The challenges gradually introduce concepts such as:

- Linux command-line basics
- File and directory management
- File permissions
- Searching and filtering files
- Hidden files
- SSH
- Text processing
- Encoding and decoding
- Compression and decompression
- Archives
- Hex dumps
- Basic scripting and problem solving

Each level builds on knowledge from previous levels.

## Approach and Strategy

My general approach for solving each level is:

1. Read the level objective carefully.
2. Identify what information or file needs to be investigated.
3. Use Linux commands to inspect the environment.
4. Determine the file type or format when necessary.
5. Search, decode, decompress, or extract the required information.
6. Obtain the password for the next level.
7. Document the commands and concepts learned.

The goal is not only to complete the level, but also to understand **why the commands work and when they can be useful**.

## Progress

| Level | Status | Main Concepts |
|------|--------|---------------|
| 0 → 1 | ✅ Completed | SSH, basic Linux commands |
| 1 → 2 | ✅ Completed | File names and `cat` |
| 2 → 3 | ✅ Completed | Spaces in file names |
| 3 → 4 | ✅ Completed | Hidden files |
| 4 → 5 | ✅ Completed | File types |
| 5 → 6 | ✅ Completed | Finding files |
| 6 → 7 | ✅ Completed | File permissions and `find` |
| 7 → 8 | ✅ Completed | `grep` and searching |
| 8 → 9 | ✅ Completed | `sort`, `uniq` |
| 9 → 10 | ✅ Completed | `strings` and binary data |
| 10 → 11 | ✅ Completed | Base64 |
| 11 → 12 | ✅ Completed | ROT13 |
| 12 → 13 | ✅ Completed | Hex dump, compression and archives |

## Notes & Lessons Learned

Some important concepts I have learned so far:

- SSH is used to securely connect to remote systems.
- Linux commands can be combined to solve problems efficiently.
- `ls`, `cd`, `cat`, `file`, `find`, and `grep` are essential command-line tools.
- Hidden files can be identified using `ls -la`.
- The `file` command helps identify unknown file formats.
- Different compression formats require different tools.
- `strings` can extract readable text from binary files.
- Base64 is an encoding method, not encryption.
- ROT13 is a simple substitution cipher.
- Hex dumps can be converted back into binary data.
- Archives may contain multiple layers of compressed or archived data.
- Understanding file formats is important when investigating unknown files.

## Why I Created This Repository

I created this repository to:

- Track my progress through OverTheWire Bandit.
- Practice Linux and cybersecurity concepts.
- Improve my command-line skills.
- Document useful commands for future reference.
- Build a practical cybersecurity learning portfolio.

## Conclusion

The Bandit wargame has helped me become more comfortable with the Linux command line and taught me how to approach technical problems step by step.

I will continue updating this repository as I progress through the remaining levels.

**Current Progress: Level 0 → Level 12 completed.**

---

### Resources

- [OverTheWire](https://overthewire.org/)
- [OverTheWire Bandit](https://overthewire.org/wargames/bandit/)
