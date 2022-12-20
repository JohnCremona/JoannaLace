# commands for recreating StPaulMSS.pdf

# create 3 pdf files for the cover (from source cover.tex using
# pdflatex), text (from the scans MMM?.jpg using convert) and notes
# (from the odt file using pandoc), then merge these (using gs).

all: StPaulMSS.pdf

sources: cover.tex MSS1.jpg MSS2.jpg MSS3.jpg MSS4.jpg  MSS5.jpg MSS6.jpg NOTES\ St.Paul\ Wed\ 18th.odt

cover.pdf: sources
	pdflatex cover

MSS.pdf: sources
	convert MSS1.jpg MSS2.jpg MSS3.jpg MSS4.jpg  MSS5.jpg MSS6.jpg MSS.pdf

notes.pdf: sources
	pandoc NOTES\ St.Paul\ Wed\ 18th.odt -o notes.pdf

StPaulMSS.pdf:	cover.pdf MSS.pdf notes.pdf
	gs -dNOPAUSE -sDEVICE=pdfwrite -sOUTPUTFILE=StPaulMSS.pdf -dBATCH cover.pdf MSS.pdf notes.pdf

clean:
	/bin/rm -f *~ *.out *.log *.aux MSS.pdf cover.pdf

