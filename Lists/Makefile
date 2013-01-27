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

C_SRCS = list.c
OBJS = $(C_SRCS:.c=.o)

.PHONY:	all clean distclean

all: $(OBJS)

clean:
	$(RM) *.o *.d

distclean: clean
	$(RM) Makefile

-include $(C_SRCS:.c=.d)

.c.d :
	$(SHELL) -ec '$(CC) -M $(CPPFLAGS) $< \
		| sed '\''s/\($*\)\.o[ :]*/\1.o $@ : /g'\'' > $@; \
		[ -s $@ ] || rm -f $@'

.c.o :
	@echo "Compiling $@..."
	$(CC) -c $(CPPFLAGS) $(CFLAGS) $< -o $@
