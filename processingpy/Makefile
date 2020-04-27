GS=/usr/local/bin/gs

# Convert text to paths using GhostScript, to block students from
# copy-pasting code from PDFs
worksheets_processingpy_nocopy.pdf: worksheets_processingpy.pdf
	$(GS) -o "$@" -dNoOutputFonts -sDEVICE=pdfwrite $<

worksheets_processingpy.pdf: worksheets_processingpy.tex
	pdflatex $<
	pdflatex $<

