# Bibliography

This repository hosts the central bibliography for numerous research projects.

The bibliography file is called ``literature.bib``. ``REGEX_FIXES.md`` provides
some regex patterns which can be used to clean up bibtex files, especially from
Mendeley.

- ``annotated_bibliography`` We maintain an annotated bibliography of useful resources for future reference.
- For proper APA citation, only capitalise the first word of the title/heading and of any subtitle/subheading as well as proper               nouns and certain other types of words. Use lowercase for everything else. (See also http://blog.apastyle.org/apastyle/2012/03/title-case-and-sentence-case-capitalization-in-apa-style.html and http://blog.apastyle.org/apastyle/2012/02/do-i-capitalize-this-word.html)
- For proper APA citation in LaTeX, you first have to specify __\usepackage{natbibapa}{apacite}__ and later __\bibliographystyle{apacite}__. You have to specify __\bibliographystyle{apacite}__ in every file that includes a \bibliography{}-command. Do not use __\bibliographystyle{apalike}__! (See also https://tex.stackexchange.com/questions/263793/what-is-the-relationship-between-natbib-apacite-package-and-apa-document-class). Moreover, you might have to delete __\usepackage{bibentry}__ (if \usepackage{bibentry} is specified more than once, all such entries have to be deleted) and __\nobibliography*__.
