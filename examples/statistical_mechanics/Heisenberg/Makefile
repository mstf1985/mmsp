# Makefile
# GNU makefile for example Heisenberg model code
# Questions/comments to gruberja@gmail.com (Jason Gruber)

# includes
incdir = ../../../include/

# compilers/flags
compiler = g++
pcompiler = mpic++
flags = -O3 -I $(incdir)
pflags = $(flags) -include mpi.h

# the program
heisenberg: heisenberg.cpp
	$(compiler) $(flags) $< -o $@ -lz

parallel: heisenberg.cpp
	$(pcompiler) $(pflags) $< -o $@ -lz

clean:
	rm -f heisenberg parallel
