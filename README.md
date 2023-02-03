# PythonInterviewSpec
Repo content for Hairun dev Q & R Interview.

## Author
Houlder Rakotoson

SPDC Project manager

## NOTE

## How to convert markdown to PDF:
######

This post reviews several methods for converting a Markdown (.md) formatted file to PDF, from UNIX or Linux machines.

## Using ```Pandoc```:
```
$ pandoc How_I_got_svg-resizer_working_on_Mac_OSX.md -s -o test1.pdf
```

## Other methods:

### GRIP
http://superuser.com/questions/689056/how-can-i-convert-github-flavored-markdown-to-a-pdf
I've had success using [grip](https://github.com/joeyespo/grip) to display markdown in Chrome and then use Chrome's "Save as PDF" option in the Print dialog.

```
pip install grip  
grip your_markdown.md
```
`grip` will render the markdown on **localhost:5000** ... - just edit away and refresh the browser. Print when ready.

This gave a more reliable representation than `pandoc` and was lighter weight than installing LaTeX (required by pandoc for pdf generation).

The print is not command line in this answer, but still found this easier/more reliable (looked 100% like Github for a long document including relatively linked images and code highlighting).


### Node.js

http://superuser.com/questions/689056/how-can-i-convert-github-flavored-markdown-to-a-pdf
You can also use Node.js based markdown-pdf

```
npm install -g markdown-pdf
markdown-pdf /path/to/markdown
```

#### Also

The GRIP results look just like GitHub README pages. The Pandoc result looks like (is) 
LaTex format. And the Node.js result is the most original looking, but slightly harder to
read than GRIP output PDF. Overall, I prefer GRIP output.
