.PHONY: all clean CLEAN rebuild dustoff
CURRDATE:=$(shell date +"%Y-%m-%d")
LATEX_FILES:=$(filter-out tikz-%.tex,$(wildcard *.tex))
TARGETS:=$(LATEX_FILES:.tex=.pdf)

$(warning LATEX_FILES = $(LATEX_FILES))
$(warning TARGETS = $(TARGETS))

all: $(TARGETS)

%.pdf: %.tex
	latexmk -lualatex $<

Erinnerungszettel-A4.tex: Erinnerung.tex Erinnerung.pdf
Erinnerungszettel-A4.pdf: Erinnerung.pdf

Erinnerung.tex: tikz-details.tex tikz-erinnerung.tex

CLEAN: clean
	rm -f -- $(TARGETS)

clean:
	rm -f -- *.atfi *.out *.aux *.log *.out *.synctex.gz *.fdb_latexmk *.fls *.synctex*

dustoff: clean

rebuild: CLEAN all
