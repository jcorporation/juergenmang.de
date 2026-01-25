---
layout: post
title: "C-Snippets"
tag: c
image: /assets/garden/c-snippets.webp
permalink: /garden/c-snippets
---

Some eventually useful c-snippets, that can be compiled as a standalone program. Most of these snippets are extracted from my other software projects.

- [GitHub Repository](https://github.com/jcorporation/c-snippets)

## levensthein.c

Fuzzy substring matching using the Levensthein distance. It adds a max distance option to the implementation to be as efficient as possible.

Reference: https://en.wikibooks.org/wiki/Algorithm_Implementation/Strings/Levenshtein_distance#C

## sylt.c

Reads and parses the binary SYLT ID3v2 tag with the help of the id3tag library. It decodes UTF8, Latin1, UTF16LE and UTF16BE.
