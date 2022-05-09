# Copyright (c) 1993-1995 Argonaut Technologies Limited. All rights reserved.
#
# $Id: makefile 1.2 1998/11/12 13:15:14 johng Exp $
# $Locker: $
#
# Makefile for BRender Framework
#
#.IMPORT: BR_SOURCE_DIR BR_MAKEFILE BR_TARGET_DIR BR_MAKE_DIR

#BR_BASE_TYPE=NONE

LIBNAME=brfw.lib

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
brbegin$(OBJ_EXT) &
brbhook$(OBJ_EXT) &
brlists$(OBJ_EXT) &
brqsort$(OBJ_EXT) &
bswap$(OBJ_EXT) &
datafile$(OBJ_EXT) &
devlist$(OBJ_EXT) &
devsetup$(OBJ_EXT) &
diag$(OBJ_EXT) &
error$(OBJ_EXT) &
file$(OBJ_EXT) &
fwsetup$(OBJ_EXT) &
genfile$(OBJ_EXT) &
image$(OBJ_EXT) &
lexer$(OBJ_EXT) &
loader$(OBJ_EXT) &
mem$(OBJ_EXT) &
object$(OBJ_EXT) &
objectc$(OBJ_EXT) &
pattern$(OBJ_EXT) &
pool$(OBJ_EXT) &
printf$(OBJ_EXT) &
register$(OBJ_EXT) &
resource$(OBJ_EXT) &
resreg$(OBJ_EXT) &
scratch$(OBJ_EXT) &
token$(OBJ_EXT) &
tokenval$(OBJ_EXT) &
assocarr$(OBJ_EXT) &
sys_conf$(OBJ_EXT) &
devquery$(OBJ_EXT)

OBJS_ASM=&
blockops$(OBJ_EXT) &
magicsym$(OBJ_EXT)

#EXPORT_INCLUDES=&
#	$(DDI_INC_DIR)/blockops.h&
#	$(DDI_INC_DIR)/brassert.h&
#	$(DDI_INC_DIR)/brddi.h&
#	$(DDI_INC_DIR)/brddi_p.h&
#	$(DDI_INC_DIR)/brexcept.h&
#	$(DDI_INC_DIR)/brhton.h&
#	$(DDI_INC_DIR)/brimage.h&
#	$(INC_DIR)/brlists.h&
#	$(DDI_INC_DIR)/datafile.h&
#	$(DDI_INC_DIR)/dataf_p.h&
#	$(DDI_INC_DIR)/dev_objs.cgh&
#	$(DDI_INC_DIR)/dev_objs.hpp&
#	$(DDI_INC_DIR)/formats.h&
#	$(DDI_INC_DIR)/lexer.h&
#	$(DDI_INC_DIR)/pretok.tok&
#	$(DDI_INC_DIR)/register.h&
#	$(DDI_INC_DIR)/shortcut.h\
#	$(DDI_INC_DIR)/timing.h\
#	$(DDI_INC_DIR)/tokenmap.h\
#	$(INC_DIR)/pretok.h\
#	$(INC_DIR)/brstdlib.h\
#


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




#default: target

#depend: pretok.c pretok.h

#.INCLUDE: $(BR_MAKE_DIR)/$(BR_MAKEFILE)

#"$(DDI_INC_DIR)/dev_objs.cgh": dev_objs.cgh
#	$(COPY_FORCE) $< $@

#"$(INC_DIR)/pretok.h": pretok.h
	$(COPY_FORCE) $< $@

# Build pre-defined token list
#
#pretok.c toktype.c pretok.h .UPDATEALL: pretok.tok
#	-$(SET_WRITEABLE) pretok.h
#	-$(SET_WRITEABLE) pretok.c
#	-$(SET_WRITEABLE) toktype.c
#	perl $(BR_MAKE_DIR)/tokgen.pl $<

#"$(DDI_INC_DIR)/pretok.tok": pretok.tok
#	$(COPY) $< $@

# Convert device classes into C headers
#
#dev_objs.cgh: dev_objs.hpp
#	-$(SET_WRITEABLE) $@
#	+$(CPP) -D__CLASSGEN__ $< | $(PERL) $(BR_MAKE_DIR)/classgen.pl $(@:b) > $@

