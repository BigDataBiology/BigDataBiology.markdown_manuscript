# Manuscript template/starter

This is a simple starter template for writing a manuscript in markdown.
It uses pandoc to convert the markdown to a docx which can be opened in Word or converted to pdf.
Converting to PDF through Word leads to a more modern looking document than converting directly from markdown to pdf (which goes through LaTeX and can sometimes lead to complicated build errors).

Two options:

1. `multi_file/`: splits up the manuscript in multiple files
2. `single_file/`: keeps the manuscript in a single file

It is a matter of personal preference which to use.

Use `make` to build.
The `Makefile`s inside each directory also illustrate all the commands needed to build the manuscript and convert between formats.
