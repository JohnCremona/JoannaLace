# commands for recreating StAnthony.pdf

# create 2 pdf files for the cover (from source cover.tex using
# pdflatex), text (from the scans HW?.jpg using convert), then merge these (using gs).

all: StAnthony.pdf

sources: cover.tex StA1.jpg StA2.jpg StA3.jpg StA4.jpg  StA5.jpg StA6.jpg StA7.jpg

cover.pdf: sources
	pdflatex cover

StA1234567.pdf: sources
	convert StA1.jpg StA2.jpg StA3.jpg StA4.jpg  StA5.jpg StA6.jpg StA7.jpg StA1234567.pdf

StAnthony.pdf: cover.pdf StA1234567.pdf
	gs -dNOPAUSE -sDEVICE=pdfwrite -sOUTPUTFILE=StAnthony.pdf -dBATCH cover.pdf StA1234567.pdf

clean:
	/bin/rm -f *~ *.out *.log *.aux StA1234567.pdf cover.pdf
