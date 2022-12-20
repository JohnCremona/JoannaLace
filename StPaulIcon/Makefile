# commands for recreating StPaulIcon.pdf and  StPaulIcon_PS.pdf

# create 2 pdf files for the main article and postscript using latex
# source files StPaulIcon.tex and StPaulIcon_PS.tex using pdflatex),
# the article including the figure IconStPaul.png.

all: StPaulIcon.pdf StPaulIcon_PS.pdf

sources: StPaulIcon.tex StPaulIcon_PS.tex IconStPaul.png

StPaulIcon.pdf: sources
	pdflatex StPaulIcon

StPaulIcon_PS.pdf: sources
	pdflatex StPaulIcon_PS

clean:
	/bin/rm -f *~ *.out *.log *.aux
