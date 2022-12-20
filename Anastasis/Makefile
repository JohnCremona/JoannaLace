# commands for recreating Anastasis.pdf

# create 1 pdf files from the latex file Anastasis.tex which includes two png files.

all: Anastasis.pdf

sources: Anastasis.tex anastasis1.png anastasis2.png

Anastasis.pdf: sources
	pdflatex Anastasis

clean:
	/bin/rm -f *~ *.out *.log *.aux

