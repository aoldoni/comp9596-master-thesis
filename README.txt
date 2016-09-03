UNSW Dissertation Cover Page for LaTeX
======================================

This is a LaTeX package providing a simple way to create a dissertation title
page for the University of New South Wales.

The latest version is available from [0], unless othervise noted.

Commands
========

A titlepage (not using the titlepage environment) can be inserted with
 \makeunswphdtitlepage

The name of the school can be specified with
 \unswschool{SCHOOL}

The degree for which this document is submitted can be specified with
 \unswdegree{DEGREE}
It default to "Doctor of Philosophy"

If the thesis is done in cotutelle, the other Uni can be introduced with
 \unswcotutelle{OTHERUNI}

A more complete front matter including all statements (originality, copyright
and authenticity) for final publication can be inserted with
 \makeunswfrontmatter

With this command, a PDF version of the Thesis/Dissertation Sheet can be
inserted at the back of the titlepage. That file can be specified with
 \unswdissertationsheet{FILENAME.pdf}

The provided thesis.tex gives an example of use.


Installation
============

The style and support files need to be in the path that LaTeX will search when
compiling your thesis.  If in doubt, consult your IT support group for further
guidance.

Unix
----

The Makefile will install all the files for you. A simple invocation of "make
install" will install the files in /usr/local/share/texmf/, in the subtree
tex/latex/unswcover. You can modify the destination by specifying the texmf tree
into which you want to install the files, e.g.,
  make install TEXMFHOME=/usr/share/texmf-site
or
  make TEXMFHOME=~/.texmf install

The first two commands will install the template globally an are likely to
require superuser rights. The latter will install the files in your user's texmf
tree. For LaTeX to properly find it afterwards, you need to set the environment
variable TEXMFHOME to point to this directory (or any other you may have
chosen).

Mac OS X
--------

Installation depends on your TeX system.

* Using teTeX/LaTeX or TeXshop from fink: The Makefile _should_ work. Just issue
a
  make TEXMFHOME=~/Library/texmf install
* Using texlive-latex from MacPorts: same as for Unix above.

Please report any issue to Olivier (see below). Contributions are welcome for
other methods to integrate this with other versions of LaTeX for OS X.

Windows
-------

Put the contents of the current directory in the directory you are working
in (or make soft links). Any MiKTeX users who would like to contribute
directions here would be welcome to do so.


Authors
=======

This cover is based on the code in Guillaume Jourjon's PhD thesis, and was
further modified and generalised for by Olivier Mehani <shtrom-ctan@ssji.net>.
There might be earlier authors whose name unfortunately have not made their way
to my ears. Please let me know.


License
=======

Copyright 2013 Olivier Mehani and previous contributors

This work may be distributed and/or modified under the
conditions of the LaTeX Project Public License, either version 1.3
of this license or (at your option) any later version.
The latest version of this license is in
http://www.latex-project.org/lppl.txt
and version 1.3 or later is part of all distributions of LaTeX
version 2005/12/01 or later.

This work has the LPPL maintenance status `maintained'.

The Current Maintainer of this work is Olivier Mehani.

This work consists of the files unswcover.sty and thesis.tex.


References
==========

[0] https://scm.narf.ssji.net/git/unswcover/
