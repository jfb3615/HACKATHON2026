PDFLATEX ?= pdflatex

.PHONY: all clean

all: report.pdf

report.pdf: report.tex
	$(PDFLATEX) -interaction=nonstopmode -halt-on-error report.tex
	$(PDFLATEX) -interaction=nonstopmode -halt-on-error report.tex

clean:
	rm -f report.aux report.log report.out report.pdf
