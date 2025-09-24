##Variables
CFLAGS=-Wall -g
CC=gcc
PROGRAM=scheduler

all: main.o list.o sched.o plot.o split.o plot.o util.o
	$(CC) $(CFLAGS) -o $(PROGRAM) main.o list.o sched.o split.o plot.o util.o

plot.o: plot.c plot.h
	$(CC) $(CFLAGS) -c -o plot.o plot.c

list.o: list.c list.h
	$(CC) $(CFLAGS) -c -o list.o list.c

sched.o: sched.c sched.h
	$(CC) $(CFLAGS) -c -o sched.o sched.c

split.o: split.c split.h list.h util.h
	$(CC) $(CFLAGS) -c -o split.o split.c

main.o: main.c split.h list.h
	$(CC) $(CFLAGS) -c -o main.o main.c

util.o: util.c util.h
	$(CC) $(CFLAGS) -c -o util.o util.c

clean:
	-rm -rf *.o $(PROGRAM) $(PROGRAM).exe gantt.plt gantt.png docs
	-rm -f test/*.png test/*.plt

install: all
	sudo cp scheduler /usr/local/bin

doc:
	doxygen
