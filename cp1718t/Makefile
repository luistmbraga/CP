file = cp1718t

tudo: $(file).tex
	lhs2TeX $(file).lhs > $(file).tex
	pdflatex $(file).tex
	atril /home/luis/Desktop/cp1718t/cp1718t/cp1718t.pdf > /dev/null 2>&1 &
	
commit:
	git commit -m "Acho que estou no caminho certo????"

push:
	git push origin master

pull:
	git pull origin master

pdf: $(file).tex
	pdflatex $(file).tex

bib: 
	bibtex $(file)

all: $(file).tex
	lhs2TeX $(file).lhs > $(file).tex
	pdflatex $(file).tex
	#bibtex $(file)
	#pdflatex $(file).tex
	#pdflatex $(file).tex

# Automatically compile what is necessary, as many times as needed.
.PHONY : rubber
rubber :
	@rubber --pdf -f $(file)

clean:
	rm -rf *.aux *.log *.bbl *.bak *.ptb *.blg *.out *.spl 

cleanall : clean
	rm $(file).pdf

