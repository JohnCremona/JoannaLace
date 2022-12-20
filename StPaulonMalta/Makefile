# commands for recreating SPoM.pdf

# create 1 pdf files from latex file + 3 jpgs

all: SPoM.pdf

sources: SPoM.tex fig1.jpg fig2.jpg fig3.jpg

SPoM.pdf: sources
	pdflatex SPoM

clean:
	/bin/rm -f *~ *.out *.log *.aux

