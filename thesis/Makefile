# makefile pro preklad LaTeX verze Bc. prace
# makefile for compilation of the thesis
# Autori / Authors: 2008 Michal Bidlo, 2016 Jaroslav Dytrych
# E-mail: dytrych AT fit vutbr cz
#===========================================
# asi budete chtit prejmenovat / you will probably rename:
CO=projekt

all: $(CO).pdf

pdf: $(CO).pdf

$(CO).ps: $(CO).dvi
	dvips $(CO)

draft: $(CO)*.tex
	pdflatex $(CO)

$(CO).pdf: clean
	pdflatex -draftmode $(CO)
	bibtex $(CO)
	pdflatex -draftmode $(CO)
	pdflatex $(CO)
	cp $(CO).pdf ../PDF/thesis.pdf
	cp zadani.pdf ../PDF/assignment.pdf

$(CO).dvi: $(CO).tex $(CO).bib
	latex $(CO)
	bibtex $(CO)
	latex $(CO)
	latex $(CO)

clean:
	rm -f *.dvi *.log $(CO).blg $(CO).bbl $(CO).toc *.aux $(CO).out $(CO).lof $(CO).ptc
	rm -f $(CO).pdf
	rm -f *~

pack:
	tar czvf $(CO).tar.gz *.tex *.bib *.bst ./template-fig/* ./bib-styles/* ./cls/* zadani.pdf $(CO).pdf Makefile Changelog

rename:
	mv $(CO).tex $(NAME).tex
	mv $(CO)-01-kapitoly-chapters.tex $(NAME)-01-kapitoly-chapters.tex
	mv $(CO)-20-literatura-bibliography.bib $(NAME)-20-literatura-bibliography.bib
	mv $(CO)-30-prilohy-appendices.tex $(NAME)-30-prilohy-appendices.tex
	mv $(CO)-40-rozsirenyabstrakt-extendedabstract.tex $(NAME)-40-rozsirenyabstrakt-extendedabstract.tex
	sed -i "s/$(CO)-01-kapitoly-chapters/$(NAME)-01-kapitoly-chapters/g" $(NAME).tex
	sed -i "s/$(CO)-20-literatura-bibliography/$(NAME)-20-literatura-bibliography/g" $(NAME).tex
	sed -i "s/$(CO)-30-prilohy-appendices/$(NAME)-30-prilohy-appendices/g" $(NAME).tex
	sed -i "s/$(CO)-40-rozsirenyabstrakt-extendedabstract/$(NAME)-40-rozsirenyabstrakt-extendedabstract/g" $(NAME).tex
	sed -i "s/$(CO)/$(NAME)/g" Makefile

# Pozor, vlna neresi vse (viz popis.txt) / Warning - vlna is not solving all problems (see description.txt)
vlna:
	vlna -l $(CO)-*.tex

# Spocita normostrany / Count of standard pages
normostrany:
	@echo "scale=2; `detex -n $(CO)-[01]*.tex | wc -c`/1800;" | bc

# Spocita normostrany rozsireneho abstractu / Count of standard pages of extended abstract
normostrany-extabs:
	@echo "scale=2; `detex -n $(CO)-[4]*.tex | wc -c`/1800;" | bc
