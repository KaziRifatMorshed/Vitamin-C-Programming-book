# Vitamin-C-Programming-book

Supplement like C Programming guide book for beginners\
Link: <https://kazirifatmorshed.github.io/Vitamin-C-Programming-book/>
\
\
![book banner](./src/Vitamin-C-programming-supplement.webp)

# How to contribute

**It is prerequisite to have knowledge of markdown and GitHub. SUMMARY.md file is used as the Contents(সূচিপত্র). If you want to add a new file (as a new chapter), edit this SUMMARY.md file and put your new '.md' file in respective place. If you want to edit content of any file, go ahead. Fork the repository and push your commit.**

```bash
Vitamin-C-Programming-book/
├── book
└── src
    ├── chapter_1.md
    └── SUMMARY.md
```

* The `src` directory is where you write your book in markdown. It contains all
  the source files, configuration files, etc.

* The `book` directory is where your book (html) is rendered. All the output is ready
  to be uploaded to a server to be seen by your audience.

* The `SUMMARY.md` is the skeleton of your
  book, and is discussed in more detail [in another
  chapter](../format/summary.md).

#### Tip: Generate chapters from SUMMARY.md

`SUMMARY.md` file allows you to think and create the whole structure of your book and then
let mdBook generate it for you. It is the summary file located at src/SUMMARY.md. This file contains a list of all the chapters in the book. Before a chapter can be viewed, it must be added to this list.

Here’s a basic summary file with a few chapters:

```
# Summary

[Introduction](README.md)

- [My First Chapter](my-first-chapter.md)
- [Nested example](nested/README.md)
    - [Sub-chapter](nested/sub-chapter.md)
```

Try opening up src/SUMMARY.md in your editor and adding a few chapters. If any of the chapter files do not exist, mdbook will automatically create them for you.

## SUMMARY.md

The summary file is used by mdBook to know what chapters to include, in what
order they should appear, what their hierarchy is and where the source files
are. Without this file, there is no book.

This markdown file must be named `SUMMARY.md`. Its formatting
is very strict and must follow the structure outlined below to allow for easy parsing. Any element not specified below, be it formatting or textual, is likely to be ignored at best, or may cause an error when attempting to build the book.

### Structure

1. ***Title*** - While optional, it's common practice to begin with a title, generally <code
   class="language-markdown"># Summary</code>. This is ignored by the parser however, and
   can be omitted.

   ```markdown
   # Summary
   ```

2. ***Prefix Chapter*** - Before the main numbered chapters, prefix chapters can be added
   that will not be numbered. This is useful for forewords,
   introductions, etc. There are, however, some constraints. Prefix chapters cannot be
   nested; they should all be on the root level. And you cannot add
   prefix chapters once you have added numbered chapters.

   ```markdown
   [A Prefix Chapter](relative/path/to/markdown.md)

   - [First Chapter](relative/path/to/markdown2.md)
   ```

3. ***Part Title*** -
   Level 1 headers can be used as a title for the following numbered chapters.
   This can be used to logically separate different sections of the book.
   The title is rendered as unclickable text.
   Titles are optional, and the numbered chapters can be broken into as many parts as desired.
   Part titles must be h1 headers (one `#`), other heading levels are ignored.

   ```markdown
   # My Part Title

   - [First Chapter](relative/path/to/markdown.md)
   ```

4. ***Numbered Chapter*** - Numbered chapters outline the main content of the book
   and can be nested, resulting in a nice hierarchy
   (chapters, sub-chapters, etc.).

   ```markdown
   # Title of Part

   - [First Chapter](relative/path/to/markdown.md)
   - [Second Chapter](relative/path/to/markdown2.md)
     - [Sub Chapter](relative/path/to/markdown3.md)

   # Title of Another Part

   - [Another Chapter](relative/path/to/markdown4.md)
   ```

   Numbered chapters can be denoted with either `-` or `*` (do not mix delimiters).

5. ***Suffix Chapter*** - Like prefix chapters, suffix chapters are unnumbered, but they come after
   numbered chapters.

   ```markdown
   - [Last Chapter](relative/path/to/markdown.md)

   [Title of Suffix Chapter](relative/path/to/markdown2.md)
   ```

6. ***Draft chapters*** - Draft chapters are chapters without a file and thus content.
   The purpose of a draft chapter is to signal future chapters still to be written.
   Or when still laying out the structure of the book to avoid creating the files
   while you are still changing the structure of the book a lot.
   Draft chapters will be rendered in the HTML renderer as disabled links in the table
   of contents, as you can see for the next chapter in the table of contents on the left.
   Draft chapters are written like normal chapters but without writing the path to the file.

   ```markdown
   - [Draft Chapter]()
   ```

7. ***Separators*** - Separators can be added before, in between, and after any other element. They result
   in an HTML rendered line in the built table of contents. A separator is
   a line containing exclusively dashes and at least three of them: `---`.

   ```markdown
   # My Part Title

   [A Prefix Chapter](relative/path/to/markdown.md)

   ---

   - [First Chapter](relative/path/to/markdown2.md)
   ```

***

## Contributors

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->

<!-- prettier-ignore-start -->

<!-- markdownlint-disable -->

<!-- markdownlint-restore -->

<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

***

[Kazi Rifat Morshed](https://kazirifatmorshed.github.io)\
KU CSE 230220
