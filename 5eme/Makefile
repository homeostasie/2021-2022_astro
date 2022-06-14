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
FIGSRC = $(wildcard 5x2-symetrie-centrale/*.ipe 5x3-triangles/*.ipe 5x4-relatifs/*.ipe 5x5-aires-et-perimetres/* 5x8-angles/*.ipe)

FIGOBJ = $(FIGSRC:.ipe=.pdf)

img: $(FIGOBJ)

5x2-symetrie-centrale/%.pdf: 5x2-symetrie-centrale/%.ipe
	ipetoipe -pdf $<
5x3-triangles/%.pdf: 5x3-triangles/%.ipe
	ipetoipe -pdf $<
5x4-relatifs/%.pdf: 5x4-relatifs/%.ipe
	ipetoipe -pdf $<
5x4-relatifs/%.pdf: 5x4-relatifs/%.ipe
	ipetoipe -pdf $<
5x5-aires-et-perimetres/%.pdf: 5x5-aires-et-perimetres/%.ipe
	ipetoipe -pdf $<
5x8-angles/%.pdf: 5x8-angles/%.ipe
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

2ie:
	pdflatex 5x2-symetrie-centrale/5x2-ie.tex
	pdflatex 5x2-symetrie-centrale/5x2-ie.tex
	mv 5x2-ie.pdf '$(PDFDIR)'/5x2-ie-sym.pdf

3c:
	pdflatex 5x3-triangles/5x3-cours.tex
	pdflatex 5x3-triangles/5x3-cours.tex
	mv 5x3-cours.pdf '$(PDFDIR)'/5x3-cours-triangles.pdf

3ie:
	pdflatex 5x3-triangles/5x3-ie.tex
	pdflatex 5x3-triangles/5x3-ie.tex
	mv 5x3-ie.pdf '$(PDFDIR)'/5x3-ie-triangles.pdf

4c:
	pdflatex 5x4-relatifs/5x4-cours.tex
	pdflatex 5x4-relatifs/5x4-cours.tex
	mv 5x4-cours.pdf '$(PDFDIR)'/5x4-cours-relatifs.pdf

4exo:
	pdflatex 5x4-relatifs/5x4-exo.tex
	pdflatex 5x4-relatifs/5x4-exo.tex
	mv 5x4-exo.pdf '$(PDFDIR)'/5x4-exo-relatifs.pdf	
	
4ie:
	pdflatex 5x4-relatifs/5x4-ie.tex
	pdflatex 5x4-relatifs/5x4-ie.tex
	mv 5x4-ie.pdf '$(PDFDIR)'/5x4-ie-relatifs.pdf

5ie:
	pdflatex 5x5-aires-et-perimetres/5x5-ie.tex
	pdflatex 5x5-aires-et-perimetres/5x5-ie.tex
	mv 5x5-ie.pdf '$(PDFDIR)'/5x5-ie-aires-et-perimetres.pdf		
	
6c:
	pdflatex 5x6-calcul-litteral/5x6-cours.tex
	pdflatex 5x6-calcul-litteral/5x6-cours.tex
	mv 5x6-cours.pdf '$(PDFDIR)'/5x6-cours-calcul-litteral.pdf

6pie:
	pdflatex 5x6-calcul-litteral/5x6-prog-ie.tex
	pdflatex 5x6-calcul-litteral/5x6-prog-ie.tex
	mv 5x6-prog-ie.pdf '$(PDFDIR)'/5x6-prog-ie.pdf

6ie:
	pdflatex 5x6-calcul-litteral/5x6-ie.tex
	pdflatex 5x6-calcul-litteral/5x6-ie.tex
	mv 5x6-ie.pdf '$(PDFDIR)'/5x6-ie-calcul-litteral.pdf

7c:
	pdflatex 5x7-fractions/5x7-cours.tex
	pdflatex 5x7-fractions/5x7-cours.tex
	mv 5x7-cours.pdf '$(PDFDIR)'/5x7-cours-fractions.pdf

7ie:
	pdflatex 5x7-fractions/5x7-ie.tex
	pdflatex 5x7-fractions/5x7-ie.tex
	mv 5x7-ie.pdf '$(PDFDIR)'/5x7-ie-fractions.pdf	

8ie:
	pdflatex 5x8-angles/5x8-ie.tex
	pdflatex 5x8-angles/5x8-ie.tex
	mv 5x8-ie.pdf '$(PDFDIR)'/5x8-ie-angles.pdf

9ie:
	pdflatex 5x9-negatifs/5x9-ie.tex
	pdflatex 5x9-negatifs/5x9-ie.tex
	mv 5x9-ie.pdf '$(PDFDIR)'/5x9-ie-negatifs.pdf


10ie:
	pdflatex 5x10-statistiques/5x10-ie.tex
	pdflatex 5x10-statistiques/5x10-ie.tex
	mv 5x10-ie.pdf '$(PDFDIR)'/5x10-ie-statistiques.pdf

11ie:
	pdflatex 5x11-proportionnalite/5x11-ie.tex
	pdflatex 5x11-proportionnalite/5x11-ie.tex
	mv 5x11-ie.pdf '$(PDFDIR)'/5x11-ie-proportionnalite.pdf


# nettoyage		
proper:
	rm -f *.log *.toc *.aux *.nav *.snm *.out *.bbl *.blg *.dvi *.ps
	rm -f *.backup *~