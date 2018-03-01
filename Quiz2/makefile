# Make files
#
# Written by Brodey R. Dickerson

CC = g++
CFLAGS = -g -Wall

all: build doczip

clean:
	rm -f myexe *out *class *.o *~

build: myexe

myexe: collegemain.o course.o college.o
	$(CC) $(CFLAGS) collegemain.o course.o college.o -o myexe

collegemain.o: course.h node.h college.h tarray.h collegemain.cc
	$(CC) -c $(CFLAGS) collegemain.cc

college.o: course.h node.h college.h college.cc
	$(CC) -c $(CFLAGS) college.cc

course.o: course.h course.cc
	$(CC) -c $(CFLAGS) course.cc

doczip: course.h course.cc node.h college.h college.cc tarray.h collegemain.cc html latex 2401fal15proj3.doc
	tar -cvf quiz2.tar course.h course.cc node.h college.h college.cc tarray.h collegemain.cc html latex 2401fal15proj3.doc