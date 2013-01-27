# Generated automatically from Makefile.in by configure.
#------------------------------------------------------------------------------
#
# CHARITY MAKEFILE
#
#------------------------------------------------------------------------------

SRCDIR=..
CC=gcc
LEX=flex
YACC=bison -y

INC=$(SRCDIR)/Include

CFLAGS=-g -O2 -DNDEBUG 
CPPFLAGS= -I$(INC)

# THE OBJECT FILES

C_SRCS = commands.c ioChar.c lib.c main.c pmem.c
OBJS = $(C_SRCS:.c=.o)

.PHONY:	all clean distclean

-include $(C_SRCS:.c=.d)

all: $(OBJS)

clean:
	$(RM) *.o *.d

distclean:
	$(RM) Makefile
	
.c.d :
	$(SHELL) -ec '$(CC) -M $(CPPFLAGS) $< \
		| sed '\''s/\($*\)\.o[ :]*/\1.o $@ : /g'\'' > $@; \
		[ -s $@ ] || rm -f $@'

.c.o :
	@echo "Compiling $@..."
	$(CC) -c $(CPPFLAGS) $(CFLAGS) $< -o $@
