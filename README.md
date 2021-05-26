# python-pdf
A command-line tool to make the core functionality of [PyPDF2](https://github.com/mstamy2/PyPDF2) interactive.

## SET-UP
I follow the set-up for python-based command-line tools outlined [here](https://dbader.org/blog/how-to-make-command-line-commands-with-python):

First, create a new directory called `~/bin` in your home directory with the following:
```
$ mkdir -p ~/bin 
```
Next, add `~/bin` to your `PATH` by adding the following line to your `.bash_profile` file (or equivalent):
```shell
export PATH=$PATH":$HOME/bin"
```
Now, download and copy the script `pypdf` to `~/bin`.

And finally, `cd` to `~/bin` and make sure `pypdf` is executable with the following:
```
$ chmod +x pypdf
```

## USAGE
**Merging PDFs**: append `file_2.pdf` to the end of `file_1.pdf` and store it in a new file called `new.pdf`.
```
$ pypdf merge new.pdf path_1/file_1.pdf path_2/file_2.pdf
```
**Splitting PDFs**: split `file.pdf` on the `n`th page into two new PDFs.
```
$ pypdf split path/file.pdf n
```
**Get PDF info**: print info about each PDF.
```
$ pypdf info path_1/file_1.pdf ... path_n/file_n.pdf
```
**Encrypt PDFs**: user will be prompted for a new password for each PDF.
```
$ pypdf encrypt path_1/file_1.pdf ... path_n/file_n.pdf
```
**Rotate pages of PDFs**: rotate all the pages of `file.pdf` 90 degrees clockwise.
```
$ pypdf rotate path/file.pdf
```
