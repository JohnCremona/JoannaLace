# commands for recreating ArchMich.pdf

# create 2 pdf files for the cover (from source cover.tex using
# pdflatex), text (from the scans AM?.jpg using convert), then merge these (using gs).

all: ArchMich.pdf

sources: cover.tex AM1.jpg AM2.jpg AM3.jpg AM4.jpg  AM5.jpg AM6.jpg AM7.jpg

cover.pdf: sources
	pdflatex cover

AM1234567.pdf: sources
	convert AM1.jpg AM2.jpg AM3.jpg AM4.jpg  AM5.jpg AM6.jpg AM7.jpg AM1234567.pdf

ArchMich.pdf: cover.pdf AM1234567.pdf
	gs -dNOPAUSE -sDEVICE=pdfwrite -sOUTPUTFILE=ArchMich.pdf -dBATCH cover.pdf AM1234567.pdf

clean:
	/bin/rm -f *~ *.out *.log *.aux AM1234567.pdf cover.pdf

