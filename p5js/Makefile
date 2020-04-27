GS=/usr/local/bin/gs

# Convert text to paths using GhostScript, to block students from
# copy-pasting code from PDFs
worksheets_p5js_nocopy.pdf: worksheets_p5js.pdf
	$(GS) -o "$@" -dNoOutputFonts -sDEVICE=pdfwrite $<

worksheets_p5js.pdf: worksheets_p5js.tex
	pdflatex $<
	pdflatex $<

