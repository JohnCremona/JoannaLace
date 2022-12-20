# commands for recreating retable.pdf

# create 1 pdf files for the main article using latex source file
# retable.tex using pdflatex, the article including figures front.png
# (frontispiece), plan.png (diagram) and 50 figures fig1.png -
# fig50.png. The png files are in subdirectory pics.

all: retable.pdf

figures: pics/fig10.png  pics/fig16.png  pics/fig21.png  pics/fig27.png  pics/fig32.png  pics/fig38.png\
	pics/fig43.png  pics/fig49.png  pics/fig8.png pics/fig11.png  pics/fig17.png  pics/fig22.png\
	pics/fig28.png  pics/fig33.png  pics/fig39.png  pics/fig44.png  pics/fig4.png   pics/fig9.png\
	pics/fig12.png  pics/fig18.png  pics/fig23.png  pics/fig29.png  pics/fig34.png  pics/fig3.png\
	pics/fig45.png  pics/fig50.png pics/fig13.png  pics/fig19.png  pics/fig24.png  pics/fig2.png\
	pics/fig35.png  pics/fig40.png  pics/fig46.png  pics/fig5.png pics/fig14.png  pics/fig1.png\
	pics/fig25.png  pics/fig30.png  pics/fig36.png  pics/fig41.png  pics/fig47.png  pics/fig6.png\
	pics/fig15.png  pics/fig20.png  pics/fig26.png  pics/fig31.png  pics/fig37.png  pics/fig42.png\
	pics/fig48.png  pics/fig7.png\
	pics/front.png pics/plan.png

sources: retable.tex figures

retable.pdf: sources
	pdflatex retable

clean:
	/bin/rm -f *~ *.out *.log *.aux
