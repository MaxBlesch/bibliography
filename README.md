# Bibliography

This repository hosts the central bibliography for numerous research projects.

The bibliography file is called `literature.bib`. 

- For proper APA citation, only capitalise the first word of the title/heading and of any subtitle/subheading as well as proper nouns and certain other types of words. Use lowercase for everything else (for more details see section **Sentence Case** in the first blog post below).
- See also:
  - [APA Style 6th Edition Blog: Title Case and Sentence Case Capitalization in APA Style](https://blog.apastyle.org/apastyle/2012/03/title-case-and-sentence-case-capitalization-in-apa-style.html)
  - [APA Style 6th Edition Blog: Do I Capitalize This Word?](https://blog.apastyle.org/apastyle/2012/02/do-i-capitalize-this-word.html)

The necessary commands for proper APA citation in LaTeX seem to differ between operating systems.

## Necessary Commands for `header.tex`

### Windows and Ubuntu

```latex
\usepackage{apacite}
```

### Mac

```latex
\RequirePackage{bibentry}
\makeatletter\let\saved@bibitem\@bibitem\makeatother
\usepackage [apaciteclassic]{apacite}
\usepackage{notoccite}
\usepackage{bibentry}
```

## Necessary Commands for `main.tex` (All Systems)

  - `\bibliographystyle{apacite}`
  - `\bibliography {../../../submodules/bibliography/literature}` or similar, depending on the location of the submodule directory relative to your `main.tex` file.

## Notes for JabRef Users

- If you want to insert a new entry in `literature.bib` via JabRef, please do not insert the BibtexKey manually but instead follow the following steps:

  - Go to **Options** -> **Preferences** -> **BibTeX key generator**
  - Insert `[auth].[year]` as the default pattern
  - Check the box **Generate keys before saving (for entries without a key)**

This will create the keys automatically and in compliance with the other entries in `literature.bib`.

