# REV08 Tue Dec 10 10:39:18 WIB 2019
# REV07 Tue Sep 17 12:18:24 WIB 2019
# REV06 Tue Feb 26 12:17:00 WIB 2019
# REV04 Tue Sep 25 12:03:44 WIB 2018
# REV02 Mon Sep 18 09:08:32 WIB 2017
# START Tue Sep 13 11:44:18 WIB 2016

CC            = gcc
CPP           = cpp
CFLAGS        = -std=gnu99
LDFLAGS       = 
CPPFLAGS      =
DEPFLAGS      = -MM -MT $(@:.d=.o) 
OUTPUT_OPTION = -o $@
COMPILE       = $(CC) $(DEPFLAGS) $(CFLAGS) $(CPPFLAGS) -c
SRCS          = $(wildcard *.c)
OBJ           = $(SRCS:.c=.o)
DEP           = $(OBJ:.o=.d)
PROGS         = $(SRCS:.c=  )

P00=00-hallo
P01=01-printf-int
P02=02-printf-etc
P03=03-loop
P04=04-argc-argv
P05=05-envp
P06=06-scan
P07=07-status
P08=08-pointer
P09=09-function
P10=10-uts171
P11=11-uts172
P12=12-uts181
P13=13-uts182
P14=14-uts191


EXECS= \
   $(P00) \
   $(P01) \
   $(P02) \
   $(P03) \
   $(P04) \
   $(P05) \
   $(P06) \
   $(P07) \
   $(P08) \
   $(P09) \
   $(P10) \
   $(P11) \
   $(P12) \
   $(P13) \
   $(P14) \


DEMOFILES=\
	demo.txt \
        

MODE644=\
	demo.txt \


all:  $(EXECS) demo.txt

$(EXECS): %: %.c $(DEPS)
	$(CC) $(CFLAGS) $< -o $@ $(LDFLAGS)

.phony: clean demo

clean:
	rm -f ${EXECS} 
	rm -f ${DEMOFILES}
	rm -f *.map
 
demo: demo.txt
demo.txt:
	@echo "Line 1: Blah Blah Blah 1" >  demo.txt
	@echo "Line 2: Blah Blah Blah 2" >> demo.txt
	@echo "Line 3: Blah Blah Blah 3" >> demo.txt
	@chmod 644 $(MODE644)


