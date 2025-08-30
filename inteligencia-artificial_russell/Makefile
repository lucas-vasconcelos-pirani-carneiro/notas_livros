# Nome do PDF final
PDFNAME   = anotacoes

# Nome do arquivo principal do LaTeX
TEX       = main.tex

# Diretório de saída
OUTDIR    = compilados

# Regra padrão
all: $(OUTDIR)/$(PDFNAME).pdf

# Compila o tex e move para compilados/
$(OUTDIR)/$(PDFNAME).pdf: $(TEX)
	mkdir -p $(OUTDIR)
	pdflatex $(TEX)
	mv main.pdf $(OUTDIR)/$(PDFNAME).pdf

# Limpa arquivos temporários do LaTeX
clean:
	rm -f *.aux *.log *.out *.toc *.synctex.gz *.fls *.fdb_latexmk *.bbl *.blg

# Limpa tudo (inclusive PDFs gerados)
cleanall:
	rm -f *.aux *.log *.out *.toc *.synctex.gz *.fls *.fdb_latexmk *.bbl *.blg
	rm -rf $(OUTDIR)/*.pdf

.PHONY: all clean cleanall
