all: dynamic_block static_block
clean:
	rm *.o *.so dynamic_block static_block

dynamic_block: program.o libDblock.so
	cc program.o libDblock.so -o dynamic_block -Wl,-rpath .


static_block: program.o libSblock.a
	cc program.o libSblock.a -o static_block

program.o: program.c
	cc -c program.c -o program.o

block.o: source/block.c headers/block.h
	cc -c source/block.c -o block.o

libDblock.so: block.o
	cc -shared -o libDblock.so block.o
 
libSblock.a: block.o
	ar qc libSblock.a block.o

block.o: headers/block.h
