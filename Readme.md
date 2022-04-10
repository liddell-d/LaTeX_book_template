#### Synopsis

LaTeX Book Template. Initial version, July 2021.

This directory consists of a template for the LaTeX book class and contains files corresponding to sections commonly found in books. The template is in a ready-to-run configuration for PdfLaTeX and related rendering engines.

#### File Organization

The primary file (containing the preamble) is _book.tex_. It is fairly well commented, so the purposes of things in it are relatively apparent. As always, details can be found in package documentation on CTAN or in your LaTeX installation.

The compiled glossary, bibliography, and index files have been included and can be recompiled as needed. The bibliography database file is in the backmatter subdirectory.

The subdirectories are named in an obvious way that corresponds to the main divisions of the book class. Files belonging to these divisions are in the respective subdirectories.

#### Formatting Notes

Some notes about page layout choices, which are simply matters of taste. 

Most of the choices mentioned here that are overrides of default behaviors are configured in the _book.tex_ file and are commented for easy reference. In some cases, however, the overrides occur in \include files. Simply comment out overrides to restore default behaviors.

Automatically generated pages having no content in their bodies are rendered as blank by the emptypage package. This is not a default.

Certain files in the frontmatter and backmatter contain the \pagestyle{empty} option, which disables headers, footers, and page numbers in the pages generated from these files.

The page numbers in the frontmatter are lowercase Roman numerals and centered in the page bottoms. This is the default. This is also done for the page numbers in the backmatter, which is not the default, although this lends a certain symmetry to the overall pagination scheme. Page numbers in the mainmatter section appear as Arabic numerals in the corners of the page bottoms. The default is centered.

The header font throughout is sans-serif. The default is Roman. This override applies to headers of all types, including captions, and to all auto-generated sections like the TOC, index, and so forth.

Page headers have bold chapter names in mixed-case letters in right-facing pages and italic section names in left-facing pages. This is not the default.

Enumeration of chapters and sections, something appropos to technical works, in addition to being a default behavior, has been suppressed. To disable this override, comment out this line in _book.tex_:

        \setcounter{secnumdepth}{-1}


