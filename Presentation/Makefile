# commands for recreating Presentation.pdf

# create 2 pdf files for the cover (from source cover.tex using
# pdflatex), text (from the scans HW?.jpg using convert), then merge these (using gs).

all: Presentation.pdf

sources: cover.tex Pres1.jpg Pres2.jpg Pres3.jpg Pres4.jpg  Pres5.jpg Pres6.jpg

cover.pdf: sources
	pdflatex cover

Pres123456.pdf: sources
	convert Pres1.jpg Pres2.jpg Pres3.jpg Pres4.jpg  Pres5.jpg Pres6.jpg Pres123456.pdf

Presentation.pdf: cover.pdf Pres123456.pdf
	gs -dNOPAUSE -sDEVICE=pdfwrite -sOUTPUTFILE=Presentation.pdf -dBATCH cover.pdf Pres123456.pdf

clean:
	/bin/rm -f *~ *.out *.log *.aux Pres123456.pdf cover.pdf
