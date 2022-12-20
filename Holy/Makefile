# commands for recreating HolyWomen.pdf

# create 2 pdf files for the cover (from source cover.tex using
# pdflatex), text (from the scans HW?.jpg using convert), then merge these (using gs).

all: HolyWomen.pdf

sources: cover.tex HW1.jpg HW2.jpg HW3.jpg HW4.jpg  HW5.jpg HW6.jpg

cover.pdf: sources
	pdflatex cover

HW123456.pdf: sources
	convert HW1.jpg HW2.jpg HW3.jpg HW4.jpg  HW5.jpg HW6.jpg HW123456.pdf

HolyWomen.pdf: cover.pdf HW123456.pdf
	gs -dNOPAUSE -sDEVICE=pdfwrite -sOUTPUTFILE=HolyWomen.pdf -dBATCH cover.pdf HW123456.pdf

clean:
	/bin/rm -f *~ *.out *.log *.aux HW123456.pdf cover.pdf
