BOOK=lfd
CHAPTER=01
SHOW=evince
BUILD=pdflatex
INCLUDEDIR=../common
DEPS=\
		 $(INCLUDEDIR)/MathematicsWorkbook.sty \
		 $(INCLUDEDIR)/$(BOOK).sty \


BOOKCH=$(BOOK)_ch$(CHAPTER)
TEXFILE=$(BOOKCH).tex
PDFFILE=$(BOOKCH).pdf

$(PDFFILE): $(TEXFILE) $(DEPS)
	TEXINPUTS=..//:$(TEXINPUTS) $(BUILD) $(TEXFILE)

all: show_$(BOOKCH)

show_$(BOOKCH): $(PDFFILE)
	$(SHOW) $(PDFFILE)

clean:
	rm -f *.bak *.aux *.log *.pdf *.sav *.ans *.inx *.ref
