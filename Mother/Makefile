# commands for recreating MotherChild.pdf

# create 2 pdf files for the cover (from source cover.tex using
# pdflatex), text (from the scans HW?.jpg using convert), then merge these (using gs).

all: MotherChild.pdf

sources: cover.tex Mother1.jpg Mother2.jpg Mother3.jpg Mother4.jpg  Mother5.jpg Mother6.jpg

cover.pdf: sources
	pdflatex cover

Mother123456.pdf: sources
	convert Mother1.jpg Mother2.jpg Mother3.jpg Mother4.jpg  Mother5.jpg Mother6.jpg Mother123456.pdf

MotherChild.pdf: cover.pdf Mother123456.pdf
	gs -dNOPAUSE -sDEVICE=pdfwrite -sOUTPUTFILE=MotherChild.pdf -dBATCH cover.pdf Mother123456.pdf

clean:
	/bin/rm -f *~ *.out *.log *.aux Mother123456.pdf cover.pdf
