INC=-I/usr/local/Cellar/boost/1.58.0/include -I/Users/cheng109/toberemoved/phosim/phosim_core/source/cfitsio/include -I/usr/local/include -I/Users/juncheng/work/phosim_core/source/cfitsio/include
LIB=-L/usr/local/Cellar/boost/1.58.0/lib -L/usr/local/lib -L/Users/cheng109/toberemoved/phosim/phosim_core/source/cfitsio/lib -L/Users/juncheng/work/phosim_core/source/cfitsio/lib -L/opt/local/lib

CC=g++
CFLAGS=-Wall -O2 -g
LDFLAGS=-lcfitsio -larmadillo # -lboost_iostreams -lboost_system 

#all: main.o Image.o commons.o Model.o
#	g++ $(INC) $(LIB) $(CFLAG) $(LDFLAGS) commons.cpp main.cpp Image.cpp Model.cpp -o junGL 
#	./junGL
	
all: main.cpp Image.o commons.o Model.o 
	$(CC) $(CFLAGS) $(INC) $(LIB) $(LDFLAGS) -c main.cpp
	./junGL

Image.o: Image.cpp Image.h
	$(CC) $(CFLAGS) $(INC) $(LIB) $(LDFLAGS) -c Image.cpp
	
commons.o:commons.cpp commons.h
	$(CC) $(CFLAGS) $(INC) $(LIB) $(LDFLAGS) -c commons.cpp
	
Model.o:  Model.cpp Model.h
	$(CC) $(CFLAGS) $(INC) $(LIB) $(LDFLAGS) -c Model.cpp
	
clean: #
	rm *.o junGL

