SOURCE=haskell.tex
PREFIX=../
PDFS=presentation.pdf handout.pdf notes.pdf
notes=

all: clean $(SOURCE) $(PDFS)

install: $(PDFS)
	cp -t $(PREFIX) $(PDFS)

haskell.pdf: $(SOURCE)
	

%.pdf: $(SOURCE)
ifdef notes
	sed 's@%%%withnotes%%%@@' $< >$(@:.pdf=.tex)
else
	cp $< $(@:.pdf=.tex)
endif
	sed "s@%%%$(@:.pdf=)%%%@@" $(@:.pdf=.tex) | pdflatex -halt-on-error -shell-escape --jobname $(@:.pdf=) -- >/dev/null

.PHONY : clean
clean:
	rm -f *.vrb *.out *.aux *.nav *.snm *.toc *.log *.pdf *.pyg *.tmp $(PDFS:.pdf=.tex)
