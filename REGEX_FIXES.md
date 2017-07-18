# Problem

Mendeley has an innocent option under **Tools/Option/BibTex** called *Escape
LaTex special characters (#{}%&)*. This creates a ***mess***.

Because if you export the .bib file, escape expressions are generated for every
character in the list. Note that, there were already some latex fragments in
the .bib file plus links, other expressions included characters of the list.

Do these two steps, importing, exporting, a few times and you get huge complex
latex escape expressions in bibtex entries which will eventually fail and
produce mistakes.

# Solution
First, don't tick the option. Second, I used regular expression to clean the
file from fragments. Here is the list of the expressions used:

- Escape öäü:
````
\{(\\"\{[AOUoua]\})\}
````

- Escape big letters in {}:
````
\{([A-Z])\}
````

- & character:
````
\{\\(&)\}
````
to delete escaped & and
````
\s&\s
````
to find ordinary & in citations to escape again.


- Delete whitespace string (not re):
````
{\$}{\~{}}{\$}
````

- Replace doubled curly braces around titles
````
\{\{(.*?)\}\}
````

For example, use SublimeText to search for the re in the ``.bibtex`` file and
replace with the first group ``$1``.