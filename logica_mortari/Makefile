PDFNAME   = anotacoes
TEX       = main.tex
OUTDIR    = compilados

all: $(OUTDIR)/$(PDFNAME).pdf

$(OUTDIR)/$(PDFNAME).pdf: $(TEX)
	mkdir -p $(OUTDIR)
	pdflatex $(TEX)
	mv main.pdf $(OUTDIR)/$(PDFNAME).pdf

clean:
	rm -f *.aux *.log *.out *.toc *.synctex.gz *.fls *.fdb_latexmk *.bbl *.blg

cleanall:
	rm -f *.aux *.log *.out *.toc *.synctex.gz *.fls *.fdb_latexmk *.bbl *.blg
	rm -rf $(OUTDIR)/*.pdf

.PHONY: all clean cleanall
