#
# Makefile -- build the book cover
#
# (c) 2018 Prof Dr Andreas Müller, Hochschule Rapperswil
#
all:	matrix.pdf buchcover.png front.pdf back.pdf

matrix.pdf:	matrix.tex
	pdflatex matrix.tex

buchcover.pdf:	buchcover.tex matrix.pdf
	pdflatex buchcover.tex

buchcover.png:	buchcover.pdf 
	convert -density 300 -extract 1966x2900+2630+190 buchcover.pdf \
		buchcover.png

nozzle.jpg:	nozzle.png
	convert nozzle.png -density 300 -units PixelsPerInch -flop nozzle.jpg

front.pdf:	front.tex buchcover.pdf
	pdflatex front.tex

back.pdf:	back.tex buchcover.pdf
	pdflatex back.tex
