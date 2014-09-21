# FeynCalc guide

<a href="http://feyncalc.org/">FeynCalc</a> is a Mathematica package for algebraic calculations in
elementary particle physics.

This guide is a hands-on, practical introduction to automatized 
quantum field theory calculations with FeynCalc and Mathematica.

# License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">
<img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" />
</a>

This work is licensed under a
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">
Creative Commons Attribution-ShareAlike 4.0 International License
</a>.

Copyright (C) 1990-2014 Rolf Mertig,
copyright (C) 1997-2014 Frederik Orellana,
copyright (C) 2014      Vladyslav Shtabovenko.

# Compiling the LaTeX source

## Prerequisites

- A Mathematica installation (<= 9.x)
- A recent LaTeX installation (see http://latex-project.org/ftp.html) with 

## Mathematica styles and fonts

### MacOS X:

Run the following as root - modifying the path to match your Mathematica and TeX installation.

	tar -cvzf /usr/local/texlive.orig.tar.gz /usr/local/texlive
	rsync --recursive /Applications/Mathematica.app/SystemFiles/IncludeFiles/TeX/texmf/ /usr/local/texlive/texmf-local/
	cp -i /Applications/Mathematica.app/SystemFiles/IncludeFiles/TeX/texmf/dvips/config/wolfram.map 2014/texmf-var/fonts/map/dvips/updmap/
	mktexlsr
	updmap-sys --enable Map=wolfram.map

### Linux:

Run the following - modifying the path to match your Mathematica instllation.

	cp -a /opt/Mathematica/9.0/SystemFiles/IncludeFiles/TeX/texmf ~/

### Windows:

--- not tested ---
The texmf directory of Mathematica should be put in the search path of the TeX installation.

## LaTeX invocation

	latex FCGuide.tex
	dvips FCGuide.dvi
	ps2pdf FCGuide.ps
