# commands for recreating StLawrence.pdf

# create 2 pdf files for the cover (from source cover.tex using
# pdflatex), text (using the scans fig?.jpg), then merge these (using
# gs).

all: StLawrence.pdf

sources: cover.tex StLawrence_text.tex fig1.jpg fig2.jpg fig3.jpg fig4.jpg fig5.jpg

StLawrence.pdf: sources
	pdflatex cover
	pdflatex StLawrence_text
	gs -dNOPAUSE -sDEVICE=pdfwrite -sOUTPUTFILE=StLawrence.pdf -dBATCH cover.pdf StLawrence_text.pdf

clean:
	/bin/rm -f *~ *.out *.log *.aux cover.pdf StLawrence_text.pdf
