HW_NUM = 1
COMMONLOC = $(HOME)/School/Support/LaTeX/doc-common.tex
COURSELOC = $(HOME)/School/Courses/3710.course
CONTENTLOC = $(COURSELOC)/Homework/Collection

answers$(HW_NUM).pdf: hw$(HW_NUM).tex $(COMMONLOC)
	pdflatex '\def\doccommon{$(COMMONLOC)}\def\doccontent{$(CONTENTLOC)}\def\doccourse{$(COURSELOC)}\newif\ifstandalone\standalonetrue\newif\ifanswers\answerstrue\input{hw$(HW_NUM)}'
	pdflatex '\def\doccommon{$(COMMONLOC)}\def\doccontent{$(CONTENTLOC)}\def\doccourse{$(COURSELOC)}\newif\ifstandalone\standalonetrue\newif\ifanswers\answerstrue\input{hw$(HW_NUM)}'
	mv hw$(HW_NUM).pdf answers$(HW_NUM).pdf
	pdflatex '\def\doccommon{$(COMMONLOC)}\def\doccontent{$(CONTENTLOC)}\def\doccourse{$(COURSELOC)}\newif\ifstandalone\standalonetrue\newif\ifanswers\input{hw$(HW_NUM)}'
	pdflatex '\def\doccommon{$(COMMONLOC)}\def\doccontent{$(CONTENTLOC)}\def\doccourse{$(COURSELOC)}\newif\ifstandalone\standalonetrue\newif\ifanswers\input{hw$(HW_NUM)}'

clean:
	rm *.aux *.log
