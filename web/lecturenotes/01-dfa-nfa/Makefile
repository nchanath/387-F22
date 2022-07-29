# Makefile for $(TARGET)

TARGET = main

all:
	cp ../outmode-project.tex ../outmode.tex
	make $(TARGET).pdf

print:
	cp ../outmode-print.tex ../outmode.tex
	make $(TARGET).pdf
	pdfjam --nup 1x3 --frame true --offset "-3cm 0" --scale .9 $(TARGET).pdf

$(TARGET).dvi: $(TARGET).tex ../outmode.tex
	latex $(TARGET)

ps: $(TARGET).ps

pdf: $(TARGET).pdf

$(TARGET).ps: $(TARGET).dvi $(TARGET).tex ../outmode.tex
	dvips -Ppdf -o $(TARGET).ps $(TARGET).dvi

$(TARGET).pdf: $(TARGET).ps $(TARGET).dvi $(TARGET).tex ../outmode.tex
	ps2pdf $(TARGET).ps

clean:
	rm -f main-pdfjam.pdf *.aux *.bbl *.dvi *.log *.blg *.mpx  *~ $(TARGET).pdf $(TARGET).ps *.toc *.nav *.out *.snm $(TARGET)-1x3.pdf
