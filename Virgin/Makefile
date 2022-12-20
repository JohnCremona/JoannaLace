# commands for recreating Virgin.pdf

# create 2 pdf files for the cover (from source cover.tex using
# pdflatex), text (from the scans V?.jpg using convert), then merge these (using gs).

all: Virgin.pdf

sources: cover.tex V1.jpg V2.jpg V3.jpg V4.jpg  V5.jpg V6.jpg

cover.pdf: sources
	pdflatex cover

V123456.pdf: sources
	convert V1.jpg V2.jpg V3.jpg V4.jpg  V5.jpg V6.jpg V123456.pdf

Virgin.pdf: cover.pdf V123456.pdf
	gs -dNOPAUSE -sDEVICE=pdfwrite -sOUTPUTFILE=Virgin.pdf -dBATCH cover.pdf V123456.pdf

clean:
	/bin/rm -f *~ *.out *.log *.aux V123456.pdf cover.pdf

veryclean: clean
	/bin/rm -f *.pdf
