serverCountThrees : ServerCountThrees.o readInt32BitLE.o
	cc -o serverCountThrees ServerCountThrees.o readInt32BitLE.o

ServerCountThrees.o : ServerCountThrees.c readInt32BitLE.h
	cc -c ServerCountThrees.c

readInt32BitLE.o : readInt32BitLE.c readInt32BitLE.h
	cc -c readInt32BitLE.c

clean :
	rm serverCountThrees ServerCountThrees.o readInt32BitLE.o

test : serverCountThrees
	mkdir -p bin
	cp ./serverCountThrees ./bin/serverCountThrees
	cp ./threesData.bin ./bin/threesData.bin
	./bin/serverCountThrees
