# Bibliography

This repository hosts the central bibliography for numerous research projects.

The bibliography file is called ``literature.bib``. ``REGEX_FIXES.md`` provides
some regex patterns which can be used to clean up bibtex files, especially from
Mendeley.

- ``annotated_bibliography`` We maintain an annotated bibliography of useful resources for future reference.
- For proper APA citation, only capitalise the first word of the title/heading and of any subtitle/subheading as well as proper               nouns and certain other types of words. Use lowercase for everything else. (See also http://blog.apastyle.org/apastyle/2012/03/title-case-and-sentence-case-capitalization-in-apa-style.html and http://blog.apastyle.org/apastyle/2012/02/do-i-capitalize-this-word.html)
- For proper APA citation in LaTeX, **header.tex** has to include the following commands:

  - *\RequirePackage{bibentry} *
  - *\makeatletter\let\saved@bibitem\@bibitem\makeatother *

  as well as:

  - *\usepackage [apaciteclassic]{apacite}* 
  - *\usepackage{notoccite}* 
  - *\usepackage{bibentry}* 

- The **main.tex** has to include the following commands:

  - *\bibliographystyle{apacite}*
  - *\bibliography {../../../ submodules/bibliography/literature}*
