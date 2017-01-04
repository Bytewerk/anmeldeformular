DOCS = Anmeldevorlage

all: $(addsuffix .pdf,$(DOCS))


%.pdf: %.tex tex/*
	pdflatex $<
	pdflatex $<

.PHONY: all clean spell

spell:
	find . -name '*.tex' -exec aspell --mode=tex --lang=de --personal=./aspell-dict.dat -c {} \;

clean:
	rm *.aux
	rm *.log
	rm *.out
	rm *.pdf
