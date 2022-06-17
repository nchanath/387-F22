# Makefile for $(TARGET)

TARGET = main

all:
	make $(TARGET).pdf

$(TARGET).pdf: $(TARGET).tex
	pdflatex $(TARGET).tex

clean:
	rm -f *.aux *.bbl *.dvi *.log *.blg *.mpx  *~ $(TARGET).pdf $(TARGET).ps *.toc *.nav *.out *.snm $(TARGET).ttex
