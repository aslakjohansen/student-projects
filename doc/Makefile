TARGETS = \
	SDU\ Software\ Engineering\ MSc\ Projects\ 2022\ -\ Aslak\ Johansen\ -\ Handouts.pdf \
	SDU\ Software\ Engineering\ MSc\ Projects\ 2022\ -\ Aslak\ Johansen\ -\ Presentation.pdf \



all: ${TARGETS}

clean:
	touch ${TARGETS}
	rm -f ${TARGETS}

mrproper: clean
	touch d.aux d.log d~ d.nav d.out d.snm d.toc includes.d
	rm -f *.aux *.log *~ *.nav *.out *.snm *.toc includes.*



.includes:
	rm -Rf .includes
	mkdir .includes

.includes/msc.timestamp: .includes msc_*.tex shared.tex # figs/*.svg
	cd .. ; bin/generate-tex-includes PDF doc/msc_handouts.tex doc
	touch .includes/msc.timestamp



SDU\ Software\ Engineering\ MSc\ Projects\ 2022\ -\ Aslak\ Johansen\ -\ Presentation.pdf: msc_*.tex shared.tex .includes/msc.timestamp
	pdflatex -shell-escape msc_handouts.tex
	pdflatex -shell-escape msc_handouts.tex
	mv msc_handouts.pdf SDU\ Software\ Engineering\ MSc\ Projects\ 2022\ -\ Aslak\ Johansen\ -\ Presentation.pdf

SDU\ Software\ Engineering\ MSc\ Projects\ 2022\ -\ Aslak\ Johansen\ -\ Handouts.pdf: msc_*.tex shared.tex .includes/msc.timestamp
	pdflatex -shell-escape msc_presentation.tex
	pdflatex -shell-escape msc_presentation.tex
	mv msc_presentation.pdf SDU\ Software\ Engineering\ MSc\ Projects\ 2022\ -\ Aslak\ Johansen\ -\ Handouts.pdf

