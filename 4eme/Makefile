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
FIGSRC = $(wildcard 4x3-triangles-semblables/*.ipe 5x10-angles/sources/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

4x3-triangles-semblables/%.pdf: 4x3-triangles-semblables/%.ipe
	ipetoipe -pdf $<




1ie:
	pdflatex 4x1-relatifs/4x1-ie.tex
	pdflatex 4x1-relatifs/4x1-ie.tex
	mv 4x1-ie.pdf '$(PDFDIR)'/4x1-ie-relatifs.pdf

2ie:
	pdflatex 4x2-proportionnalite/4x2-ie.tex
	pdflatex 4x2-proportionnalite/4x2-ie.tex
	mv 4x2-ie.pdf '$(PDFDIR)'/4x2-ie-proportionnalite.pdf

3c:
	pdflatex 4x3-triangles-semblables/4x3-cours.tex
	pdflatex 4x3-triangles-semblables/4x3-cours.tex
	mv 4x3-cours.pdf '$(PDFDIR)'/4x3-cours-semblables.pdf

# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~