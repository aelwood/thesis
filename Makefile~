.PHONY: clean

EXTRASTYS = abhepexpt.sty abhep.sty abmath.sty lineno.sty siunitx.sty SIunits.sty varwidth.sty

aelwoodThesis.pdf: aelwoodThesis.tex preamble.tex introduction.tex theory.tex detector.tex reconstruction.tex frontmatter.tex appendices.tex l1trig.tex eventSelection.tex backgroundPred.tex results.tex conclusion.tex backmatter.tex
	@rm -f $(EXTRASTYS)
	unzip extrastyles.zip
	@rm -f aelwoodThesis.{aux,toc,lof,lot}
	(pdflatex aelwoodThesis && bibtex aelwoodThesis && pdflatex aelwoodThesis && pdflatex aelwoodThesis) || rm -f $(EXTRASTYS) aelwoodThesis.pdf
	@rm -f aelwoodThesis.{aux,toc,lof,lot}
	@rm -f $(EXTRASTYS)

clean:
	@rm -f $(EXTRASTYS)
	@rm -f aelwoodThesis.pdf aelwoodThesis.log aelwoodThesis.aux
	@rm -f *.bbl *.blg *.lof *.cut
	@rm -f *.lot *.out *.toc
