LESSC = lessc
JADEC = jade

all: index css

index:
	$(JADEC) index.jade
css:
	$(LESSC) style.less style.css

clean:
	rm style.css index.html
