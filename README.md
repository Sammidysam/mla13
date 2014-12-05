mla13
=====

A LaTeX MLA style formatter package that allows users to create MLA style documents easily.

# How to Install #

Download the `.sty` file and place it in the texmf folder for use with all of your LaTeX file needs. If you just want to use it on one project, just place it in your project folder for local access.

An automatic installation script for Fedora Linux will be coming soon.

# How to Use #

The mla13 package does not require that you use any other packages, though it allows you to do so. The
packages that are utilized by mla13 are: geometry, babel, csquotes, biblatex, and color. In order to use the
features provided by mla13, the first thing you have to do is to use the package in your LaTeX project. To do
this use the following command:
    
    \usepackage{mla13}

## Creating Your Header ##

All MLA documents must contain the standard 5 line header that includes your name, professors name, class
name, and the date the paper was written on. To do this, no formatting work is needed, the package just
needs the values to be set and it will do all of the heavy lifting. To set the values of the variables follow the
process below:

    \firstname{Your First Name}
    \lastname{Your Last Name}
    \professor{Your Professor's Name}
    \class{The Name of Your Class}
    \title{The Title of Your Paper}

The above code simply sets all of the data values for later use in the paper.
The header will automatically be created when you type `\begin{document}`.

## Paragraph Formatting ##

Paragraph formatting is standard and coincides with the measures put in place by MLA style. The font used is Times New Roman and is of size 12. The justification is left justified.

## Citing and Sources ##

This package uses BibTeX because it is the most commonly used for bibliographies. All of your sources
should be kept in a .bib file and should be formatted to meet the BibTeX standards. To learn more about
BibTeX and its features, look at this website http://en.wikipedia.org/wiki/BibTeX. Once your file is
set up you need to tell mla13 which file to look at. To do this type the following before the begin document
section of your LaTeX project:
   
    \sources{NameOfBibFile.bib}

To cite a source, the main command that you should use is the standard cite command. This is the one
that fits with MLA citation style. Here is an example of how to use this command:

No Page Number: `\cite{Name of Source}`
Page Number: `\cite[Page]{Name of Source}`

The works cited page will automatically be created at `\end{document}` if the sources file is specified.  If not, it will not be created.

Note that Biber must be installed for BibTeX support to work correctly.

## Changing the Date of the File ##

If you want to use a date other than the current date, the only way is to manually input the correctly
formatted date using the standard date attribute provided by LaTeX. For example, place the following
before `\begin{document}`:

    \date{5 February 2013}
    
This follows the format of MLA such that:

    \date{DAY MONTH YEAR}
    
Otherwise, to use the current date, do not include the date field inside of your file.
