SOURCE   = ML_train_flow
DENSITY = 600

make:
	pdflatex $(SOURCE).tex -output-format=pdf

clean :
	bash -c "rm -f -- *.aux *.bbl *.blg *.log *.out *.toc *.synctex.gz"

png:
	make
	convert -density 600 -quality 100 $(SOURCE).pdf $(SOURCE).png
	make clean

svg:
	make
	pdf2svg $(SOURCE).pdf $(SOURCE).svg
	make clean
