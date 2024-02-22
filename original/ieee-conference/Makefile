LITMUSLATEXDIR ?= litmus-latex

export TEXINPUTS := .:$(abspath .):$(abspath $(LITMUSLATEXDIR)):$(TEXINPUTS)

# If no other target is specified on the command line make will build this one:
.DEFAULT_GOAL = all

all:
	latexmk main -shell-escape -pdf

pdflatex:
	pdflatex --shell-escape main

loop:
	latexmk main -shell-escape -pdf -pvc

clean:
	latexmk -bibtex -C
	rm -rf svg-inkscape
