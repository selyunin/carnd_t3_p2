TARGET := 05_software_requirements
TITLE_PAGE := titlepage

# change viewer to a pdf viewer of your choice
VIEWER := evince

all:
	pdflatex $(TARGET).tex
	bibtex 	 $(TARGET).aux
	pdflatex $(TARGET).tex
	pdflatex $(TARGET).tex

view:
	@$(VIEWER) $(TARGET).pdf &

archive:
	zip -r $(TARGET).zip .

cleanall:
	@rm -f $(TARGET).log $(TARGET).aux $(TARGET).pdf $(TARGET).out $(TARGET).bbl $(TARGET).blg $(TARGET).toc

clean:
	@rm -f $(TARGET).log $(TARGET).aux $(TARGET).out $(TARGET).bbl $(TARGET).blg \
		$(TARGET).toc $(TARGET).nav $(TARGET).snm $(TARGET).dvi $(TARGET).bcf  \
		$(TARGET).lof $(TARGET).lot $(TARGET).ver $(TARGET).hst \
		$(TITLE_PAGE).aux \
		$(TARGET).zip

cleanbackup:
	@rm -f $(TARGET).tex.backup $(TARGET).tex~ $(MAKE)~
	@rm -f .$(TARGET)*~ .$(MAKE)*~
