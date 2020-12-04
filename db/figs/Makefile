TARGETS = \
	privacy-analyzer.png \



all: ${TARGETS}

clean:
	touch ${TARGETS}
	rm -R ${TARGETS}

mrproper: clean
	touch d~
	rm -R *~



privacy-analyzer.png: Makefile privacy-analyzer.svg
	inkscape -C --export-type=png --export-width=820 privacy-analyzer.svg

