.PHONY: all clean CLEAN rebuild dustoff
CURRDATE:=$(shell date +"%Y-%m-%d")
LATEX_FILES:=$(wildcard *.tex)
TARGETS:=$(LATEX_FILES:.tex=.pdf)

all: $(TARGETS)

%.pdf: %.tex
	latexmk -lualatex $<

Erinnerungszettel-A4.tex: Erinnerung.pdf

CLEAN: clean
	rm -f -- $(TARGETS)

clean:
	rm -f -- *.atfi *.out *.aux *.log *.out *.synctex.gz *.fdb_latexmk *.fls *.synctex*

dustoff: clean

rebuild: CLEAN all
