FILE=presentation

make:
	@pdflatex $(FILE).tex
	@cp $(FILE).pdf ../PDF/

silent:
	@pdflatex -interaction=batchmode $(FILE).tex
	@cp $(FILE).pdf ../PDF/

clean:
	rm -f *.aux *.log *.nav *.out *.snm *.toc

travis-build: clean
	pdflatex -halt-on-error $(FILE).tex
