---
title: "Markdown languages. Markdown"
subtitle: This article includes an information about markdown languages!

# Summary for listings and search engines
summary: This article includes an information about markdown languages!

# Link this post with a project
projects: []

# Date published
date: '2023-04-01T00:00:00Z'

# Date updated
lastmod: '2023-04-01T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named featured.jpg/png in this page's folder and customize its options here.
image:
  caption: 'Image credit: **Markdown** (https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - markdown

categories:
  - Demo
---

## What are markup languages and what are they eaten with?
  
  If this is the first time you hear this phrase, then this article is definitely for you! So, a markup language (text) in computer terminology is a set of characters or sequences of characters inserted into a text to transmit information about its display or structure. Belongs to the class of computer languages. A text document written using a markup language contains not only the text itself (as a sequence of words and punctuation marks), but also additional information about its various sections — for example, an indication of titles, selections, lists, etc. In more complex cases, the markup language allows you to insert interactive elements and the contents of other documents into the document.
It should be noted that the markup language is incomplete by Turing and is not usually considered a programming language.

## Logical and visual markup
  
  There are logical and visual markup. In the first case, we are talking only about what role this section of the document plays in its overall structure (for example, "this line is the title"). In the second, it determines exactly how this element will be displayed (for example, "this line should be displayed in bold"). The idea of markup languages is that the visual representation of a document should be automatically derived from logical markup and not depend on its immediate content. This simplifies the automatic processing of the document and its display in different conditions (for example, the same file may be displayed differently on a computer screen, mobile phone and print, since the properties of these output devices differ significantly). However, this rule is often violated: for example, when creating a document in an editor like MS Word, the user can highlight the titles in bold, but not indicate anywhere that this line is the title.
  
## Examples of markup languages
  
  Markup languages are used wherever it is required to obtain formatted text based on text alone: in typography (SGML, TeX, PostScript, RTF), computer user interfaces (Microsoft Word, OpenOffice), the World Wide Web (HTML, XHTML, XML, WML, VML, PGML, SVG, XBRL). Markdown is also quite common, which will be discussed further.
  
## Markdown Syntax

Formatting of text elements in Markdown:
  
1. Headings:

To create a header, use the # sign (the number of lattices corresponds to the header level).

2. Type of font:

Bold font (** on both sides). Bold + italics (*** on both sides).

3. Quoting (>): A larger sign is placed and then a quote is written.

4. Lists:

A bulleted (unordered) list (Denoting the list items with dashes or asterisks).

Embedding lists (using indents) before each sub-item.

Ordered list (using numbers):
1.Item 1;
2. Item 2;
3. Item 3.

To nest one list into another, we also use indents.

5. Hyperlinks (the name of the link is written in square brackets, and the website is written in round brackets next to it).

6. Code design (the code is designed with the symbols ` ` above and below):

8. Design of images:
To insert an illustration into the text, you need to use the following syntax (!specify the name of the image) (Fig. @fig:001):

{#fig:001 width=70%}

