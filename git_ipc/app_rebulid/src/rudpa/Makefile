include ./Makefile.in
#SRC=$(wildcard *.c)
SRC=$(SOURCES)
OBJ=$(SRC:.c=.o)
#CFLAGS=-Wall -g3 -O0
CFLAGS= -g3 -O0 -funsigned-char
LDFLAGS= -lpthread -lrt
TAG=rudp 
ECHO =


#CROSS = arm-hisiv100nptl-linux-

CC := $(CROSS)gcc

all:$(TAG)

$(TAG):$(OBJ)
	$(CC) $(CFLAGS) $(OBJ) -o $(TAG) $(LDFLAGS)

#build the vcon's source file for test
vcon:
	$(CC) $(CFLAGS) $(LDFLAGS) -o test rudpa_vcon.c

.depend:
	$(CC) -M $(CFLAGS) $(SRC) > $@
clean:
	rm -f *.o *.d $(TAG)

#sinclude .depend
