# Copyright (c) 1993-1995 Argonaut Technologies Limited. All rights reserved.
#
# $Id: makefile 1.1 1997/12/10 17:16:27 jon Exp $
# $Locker: $
#
# Makefile for BRender foreign file format support
#
#.IMPORT: BR_SOURCE_DIR BR_MAKEFILE BR_TARGET_DIR BR_MAKE_DIR

LIBNAME=brfm
#TARGET_TYPE:=LIB

INCLUDES=-I..\..\inc -I..\inc -I..\..\ddi_inc

AS=wasm
ASFLAGS=-zq -c -DBASED_FLOAT=1 $(INCLUDES)

CC=wcc386
CFLAGS=-zq -DBASED_FLOAT=1 -DSTATIC=static 
CFLAGS+= $(INCLUDES)
CFLAGS+= -D__BR_V1DB__=0 
OBJ_EXT=.obj

LIB=wlib
LIBFLAGS=-q


## Base library object files
##
OBJS_C=&
	load3ds$(OBJ_EXT) &
	loadasc$(OBJ_EXT) &
	loadbmp$(OBJ_EXT) &
	loadgif$(OBJ_EXT) &
	loadiff$(OBJ_EXT) &
	loadnff$(OBJ_EXT) &
	loadscr$(OBJ_EXT) &
	loadtga$(OBJ_EXT) &
	savescr$(OBJ_EXT) &
        loadvue$(OBJ_EXT)

#OBJS_ASM=\


#EXPORT_INCLUDES=\
#	$(INC_DIR)/fmt.h\
#	$(INC_DIR)/fmt_p.h\


#.INCLUDE: $(BR_MAKE_DIR)/$(BR_MAKEFILE)



.c.obj:
	*$(CC) $(CFLAGS) $<

.asm.obj:
	*$(AS) $(ASFLAGS) $<

$(LIBNAME): $(OBJS_C) $(OBJS_ASM)
	*$(LIB) $(LIBFLAGS) $@ $(OBJS_C: = +-)
	*$(LIB) $(LIBFLAGS) $@ $(OBJS_ASM: = +-)
	
clean
	@DEL *.OBJ
	@DEL *.LIB

all: $(LIBNAME)