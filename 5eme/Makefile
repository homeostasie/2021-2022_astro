# Dossiers
CODE := $(shell pwd)
PDFDIR = ../_pdf/5eme
THEME = 

# Visualiser les pdf
LOG=evince

# Créer le dossier pdf s'il n'éxiste pas.
target:
	test -d $(PDFDIR) || mkdir $(PDFDIR)

all: img poly proper

# Générations des images
FIGSRC = $(wildcard 5x2-triangles/sources/*.ipe 5x10-angles/sources/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

5x2-triangles/sources/%.pdf: 5x2-triangles/sources/%.ipe
	ipetoipe -pdf $<


# Chapitre 1

1c:
	pdflatex 5x1-calculer/5x1-cours.tex
	pdflatex 5x1-calculer/5x1-cours.tex
	mv 5x1-cours.pdf '$(PDFDIR)'/5x1-cours-calculer.pdf

1d:
	pdflatex 5x1-calculer/5x1-dm.tex
	pdflatex 5x1-calculer/5x1-dm.tex
	mv 5x1-dm.pdf '$(PDFDIR)'/5x1-dm-calculer.pdf


1ie:
	pdflatex 5x1-calculer/5x1-ie.tex
	pdflatex 5x1-calculer/5x1-ie.tex
	mv 5x1-ie.pdf '$(PDFDIR)'/5x1-ie-calculer.pdf


# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~