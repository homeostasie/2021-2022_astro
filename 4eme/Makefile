# Dossiers
CODE := $(shell pwd)
PDFDIR = ../_pdf/4eme
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

4x2-triangles/sources/%.pdf: 5x2-triangles/sources/%.ipe
	ipetoipe -pdf $<


# Chapitre 1

1ie:
	pdflatex 4x1-relatifs/4x1-ie.tex
	pdflatex 4x1-relatifs/4x1-ie.tex
	mv 4x1-ie.pdf '$(PDFDIR)'/4x1-ie-relatifs.pdf

2ie:
	pdflatex 4x2-proportionnalite/4x2-ie.tex
	pdflatex 4x2-proportionnalite/4x2-ie.tex
	mv 4x2-ie.pdf '$(PDFDIR)'/4x2-ie-proportionnalite.pdf

# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~