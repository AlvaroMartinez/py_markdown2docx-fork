# py_markdown2docx-fork
This is a fork of [Markdown to Word docx](https://pypi.org/project/Markdown2docx/) file conversion from jeremy lee jlee2.71818_at_gmail_dot_com. this mod aims to overwrite some existing docx file.

**current state of devel:**  barely forked, no additional features achieved.

MIT License

# Markdown2docx

## Purpose
Markdown2docx will take a plain text markdown document and create a Word .docx file.

## Minimal Usage
```
from Markdown2docx import Markdown2docx
project = Markdown2docx('README')
project.eat_soup()
project.save()
```

You can optionally save a copy in HTML format alongside the .docx output, and print out the default styles.
```
from Markdown2docx import Markdown2docx
project = Markdown2docx('README')
project.eat_soup()
project.write_html()  # optional
print(type(project.styles()))
for k, v in project.styles().items():
    print(f'stylename: {k} = {v}')
project.save()
```

### Default styles
These are the default styles applied to the document:
```
stylename: style_table = {'Medium Shading 1 Accent 3'}
stylename: style_quote = {'Body Text'}
stylename: style_body = {'Body Text'}
stylename: style_quote_table = {'Table Grid'}
stylename: toc_indicator = {'contents'}
```

### Token substitution and commands
For details about token substitution, refer to hello.md

### Create a table of contents.
The TOC will be inserted on the first and only the first match where a paragraph contains the TOC indicator. By default this is literally the word 'contents'. When the user opens the .docx document, it will display 'Right-click to update field.'

## For developers.
Use a virtualenv. For extra dev tools, use:
bash
```
$ pip install -e .[dev]
```
### TODO
- write down objectives
- give new structure to documentation
