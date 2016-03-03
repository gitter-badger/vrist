DLIB = $(wildcard dlib-*/)

all: dlib

clean: clean-dlib

dlib: build/
	cd $^ && cmake --build . --config Release --target install

build/:
	mkdir $@
	cd $@ && cmake ../$(DLIB)/tools/python

clean-dlib: build/
	$(if $(wildcard $^), rm -r $^)
