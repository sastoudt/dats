# LaTeX

## What is in this Directory? 

### From Lawrence Lewis' talk in Spring 2014: 

There's a presentation, a document, and a poster (very alpha), which is meant to show the basics of LaTeX.

### From Katy's talk in Fall 2014

There is some information here in the readme and there are some templates in 
the templates folder. 


## What is Markup?

### HTML

HTML is just hypertext markup language. It provides a plain text way to 
describe objects and data that are encountered in the world wide web. Things 
like urls, text rendering in webpages, etc. are all easy to describe in HTML.

### XML 

XML is the extensible markup language. It generalizes where others specify. In 
the way that all reductionist things fail to get the specifics right, XML is 
great for general tasks in programming (input files, etc.), but not great for 
writing documents, where the needs are very specific. 

### MarkDown? RestructuredText? Where does it end?

There are a lot of markup languages. They all do different things. Restructured 
text is the standard in the world of python documentation. Markdown is the 
standard on github. Pick your poison.


## How Do I install LaTeX?

### Linux

Everything in linux is simple.

    sudo apt-get install texlive

### OSX

You should use [MacTeX][mactex]. You can do this with macports or homebrew by downloading the whole shabang from 
the website.

### Windows

I honestly have no idea. It [looks like][texSE] the TeX stack exchange may be able to 
help, though. 

## How do I write LaTeX?

http://tobi.oetiker.ch/lshort/lshort.pdf

### LyX

Max showed us LyX last time, which is a WYSIWYG editor for LaTeX. That's 
awesome. I recommend you give it a shot.

### TeXShop

TeXShop is something that many folks use to write and render latex side by 
side. It's cool. I don't use it, but I can see where it would be great. 

### Text Editors

Some folks will find the text editor option the most extensible and glorious. I 
am one of those folks. I have a vim plugin for latex called, you guessed it, 
vim-latex and it does most of the typing for me. With syntax highlighting, it 
tells me where there's a mistake, and by virtue of dealing directly with the 
content, I can ignore how it looks until the very end. 

## How do I pronounce LaTeX?

Check it out, the last letter is the Greek letter $$\Chi$$. So, it definitely has to 
end in a K sound. But, is it Lay or Lah? The developers say it's up to you. 

## What are the Parts of a Document?

LaTeX documents have numerous parts.

### The Preamble

In the preamble, there is a basic set of information that must be included in 
order to define the document. The real minimum set is just the "documentclass" 
parameter. Options include "article," "book," and "letter." Options concerning 
the paper format and the font can be specified in the square brackets while the 
documentclass type should be listed in the  

    \documentclass[11pt]{article}

inclusion of any packages that you rely on. Standard packages include 
"amsmath," "amsfonts," "amssymb," and graphicx. 

    \usepackage{amsmath}
    \usepackage{amssymb}

If you are expecting a title to appear, parameters such as author and title 
should be filled in. 




### begin and end

You must begin and end the document. 

    \documentclass[11pt]{article}

    \begin{document}

    <stuff>

    \end{document}


Now, that's it. To create a beautiful pdf, you can place this text in a file 
called doc.tex, type "latex doc.tex" to create a dvi file, then type dvi2pdf to 
create a pdf file.

### The Title Elements

There are elements that help to define the title elements. 


    \documentclass[11pt]{article}
    \author{The Hacker Within}
    \title{Our New Document}

    \begin{document}

    <stuff>

    \end{document}


Those variables are used by the maketitle command, which must be executed 
within the document boundaries. 


    \documentclass[11pt]{article}
    \author{The Hacker Within}
    \title{Our New Document}

    \begin{document}
    \maketitle

    \end{document}



### Books, Chapters, Sections, Subsections, Subsubsections, and Paragraphs

These are enviroments that define the hierarchy of your document. 


### Include and input

Rather than keep everything in one big file, you can include and input other 
latex files into a master. That acknowledgements section that you use in every 
paper? Keep it in its own file. 



[texSE]: http://tex.stackexchange.com/questions/41808/how-do-i-install-tex-latex-on-windows-7 "TeX Stack Exchange"
[mactex]: https://tug.org/mactex/ "mactex"
