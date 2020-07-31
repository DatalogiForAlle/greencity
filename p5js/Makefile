GS=/usr/local/bin/gs

# Convert text to paths using GhostScript, to block students from
# copy-pasting code from PDFs
worksheets_p5js_nocopy.pdf: worksheets_p5js.pdf
	$(GS) -o "$@" -dNoOutputFonts -sDEVICE=pdfwrite $<

worksheets_p5js.pdf: worksheets_p5js.tex
	pdflatex $<
	pdflatex $<

individual_files_nocopy: worksheets_p5js_nocopy.pdf
	pdftk $< cat 1-2 output arbejdsark0.pdf
	pdftk $< cat 3-4 output arbejdsark1.pdf
	pdftk $< cat 5-6 output arbejdsark2.pdf
	pdftk $< cat 7-8 output arbejdsark3.pdf
	pdftk $< cat 9-10 output arbejdsark4.pdf
	pdftk $< cat 11-12 output arbejdsark5.pdf
	pdftk $< cat 13-14 output arbejdsark6.pdf
