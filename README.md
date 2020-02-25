# git-latexdiff-rev
A wrapper for git-latexdiff. It allows you to create a pdf highlighting the changes in your latex document by specifying the commits with simple numbers and not ids. 

## Prerequisites
You have to install [git-latexdiff](https://gitlab.com/git-latexdiff/git-latexdiff) first.

## Examples
There is only one usecase, you just specify
```console
foo@bar:~$ git-latexdiff-rev -r 0,1 -i 'foo.tex'
```
and get a pdf with the differences between the current commit (0) and the commit before the current commit (1). If you need, e.g., the difference between the commit before the current commit and the and the commit before that you can use
```console
foo@bar:~$ git-latexdiff-rev -r 1,2 -i 'foo.tex'
```
and so on.

## TODO
- fix the option to save the document in case off an error in `latexdiff`
- fix the option to change the verbosity of the output
- create an option for displaying the pdf
- look for installed pdf-viewers
