# This Makefile will work only with GNU make.

CFLAGS ?= -O2 -fno-inline -g
CFLAGS += -Wall -Wstrict-prototypes
PROGRAMS = iscsi-iname

all: $(PROGRAMS)

iscsi-iname: md5.o iscsi-iname.o
	$(CC) $(CFLAGS) $(LDFLAGS) $^ $(DBM_LIB) -o $@

clean:
	$(RM) *.o $(PROGRAMS) .depend

depend:
	$(CC) $(CFLAGS) -M `ls *.c` > .depend

-include .depend
