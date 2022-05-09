# Copyright (c) 1993-1995 Argonaut Technologies Limited. All rights reserved.
#
# $Id: makefile 1.1 1997/12/10 17:16:26 jon Exp $
# $Locker: $
#
# Makefile for BRender DOS IO support libary
#
#
#.IMPORT: BR_SOURCE_DIR BR_MAKEFILE BR_TARGET_DIR BR_MAKE_DIR
#.IMPORT .IGNORE: BR_EXTENDER

BR_BASE_TYPE=NONE

INCLUDES=-I..\..\inc -I..\inc -I..\..\ddi_inc

AS=wasm
ASFLAGS=-zq -c -DBASED_FLOAT=1 $(INCLUDES)

CC=wcc386
CFLAGS=-zq -zp4 -5r -fp5 -DBASED_FLOAT=1 
CFLAGS+= $(INCLUDES)
CFLAGS+= -D__BR_V1DB__=0 
OBJ_EXT=.obj

LIB=wlib
LIBFLAGS=-q



LIBNAME=DOSIOWRR.LIB

## Base library object files
##
OBJS_C=&
divtrap$(OBJ_EXT) &
dossetup$(OBJ_EXT) &
eventq$(OBJ_EXT) &
keyboard$(OBJ_EXT) &
readmse$(OBJ_EXT)

OBJS_ASM= &
clock$(OBJ_EXT) &
divtraph$(OBJ_EXT)

#EXPORT_INCLUDES= &
#$(INC_DIR)/dosio.h &
#$(INC_DIR)/eventq.h &
#$(INC_DIR)/keyboard.h &
#$(INC_DIR)/dos_x.h &
#$(INC_DIR)/dos_p.h &

.c.obj:
	$(CC) $(CFLAGS) $<
	
.asm.obj:
	$(AS) $(ASFLAGS) $<

$(LIBNAME): $(OBJS_C) $(OBJS_ASM)
	$(LIB) $(LIBFLAGS) $@ $(OBJS_C: = +-)
	$(LIB) $(LIBFLAGS) $@ $(OBJS_ASM: = +-)

.default
all: $(LIBNAME)

clean
	DEL *.OBJ
	DEL *.LIB


#.INCLUDE: $(BR_MAKE_DIR)/$(BR_MAKEFILE)

