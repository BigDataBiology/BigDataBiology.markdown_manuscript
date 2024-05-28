all: \
    manuscript.docx \
    figure1.pdf figure1.png

%.png: %.svg
	inkscape --export-filename $@ --export-background=white --export-dpi=600 $<

%_plain.svg: %.svg
	inkscape --export-plain-svg --export-filename $@ $<

%.pdf: %.svg
	inkscape --export-filename $@ --export-dpi=600 $<

PNGS := figure1.png

manuscript.docx: manuscript.md $(PNGS)
	pandoc manuscript.md -o $@ -f markdown+smart --citeproc

manuscript_custom.docx: manuscript.md $(PNGS) custom-reference.docx
	pandoc manuscript.md -o $@ -f markdown+smart --citeproc --reference-doc=custom-reference.docx

manuscript.pdf: manuscript.docx
	libreoffice --headless --convert-to pdf $<

