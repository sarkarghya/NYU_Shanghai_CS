CFLAGS=-Iinclude -Wall
FILE=tasks
POLICY=MFQ
#POLICY values
#	FCFS
#	SJF
#	SRTF
#	RR 4
#	MFQ 3
#	IORR 4

all: build run

build: clean
	mkdir obj
	gcc $(CFLAGS) -c -o obj/policies.o src/sched-policies.c	
	gcc $(CFLAGS) -c -o obj/simulator.o src/sched-simulator.c
	mkdir bin
	gcc $(CFLAGS) -o bin/sched-simulator obj/simulator.o obj/policies.o

run:
	bin/sched-simulator $(FILE) $(POLICY) 3 >sched-run.txt
	cat *.txt

clean:
	rm -rf bin obj sched-run.txt
