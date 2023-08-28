TEXINPUTS:=.

LEC= \
	pdf/2023-08-22.pdf \
	pdf/2023-08-24.pdf \
	pdf/2023-08-29.pdf \
	pdf/2023-08-31.pdf \
	pdf/background.pdf 

.PHONY: all copy
all: $(LEC)

pdf/%.pdf: notes/%.tex common.tex
	mkdir -p pdf
	xelatex -output-dir pdf $<
	xelatex -output-dir pdf $<

clean:
	rm -f pdf/*.aux pdf/*.log pdf/*.out
	rm -f pdf/*.nav pdf/*.snm pdf/*.toc 
	rm -f pdf/*.vrb

distclean: clean
	rm -f pdf/*.pdf

copy:
	mkdir -p ../web/lec
	cp $(LEC) ../web/lec
