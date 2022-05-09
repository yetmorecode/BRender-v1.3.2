# Top level makefile for brender core libraries
#
# $Id: makefile 1.2 1998/06/30 18:15:44 johng Exp jon $
# $Locker: jon $
#
#.IMPORT: BR_SOURCE_DIR BR_MAKEFILE BR_TARGET_DIR BR_MAKE_DIR

.default
all
	cd fw
	wmake /h
	cd ..
	cd dosio
	wmake /h
	cd ..
	
clean
	cd fw
	wmake /h clean
	cd ..
	cd dosio
	wmake /h clean
	cd ..


#includes depend target clean .PHONY:
#	+$(BR_MAKE_DIR)\subdir inc       $(MAKE) $@
#	+$(BR_MAKE_DIR)\subdir fw        $(MAKE) $@
#	+$(BR_MAKE_DIR)\subdir host      $(MAKE) $@
#	+$(BR_MAKE_DIR)\subdir std       $(MAKE) $@
#	+$(BR_MAKE_DIR)\subdir pixelmap  $(MAKE) $@
#	+$(BR_MAKE_DIR)\subdir dosio     $(MAKE) $@
#	+$(BR_MAKE_DIR)\subdir v1db      $(MAKE) "BR_BASE_TYPE=FLOAT" $@
#	+$(BR_MAKE_DIR)\subdir math      $(MAKE) "BR_BASE_TYPE=FLOAT" $@
#	+$(BR_MAKE_DIR)\subdir fmt       $(MAKE) "BR_BASE_TYPE=FLOAT" $@

#    +$(BR_MAKE_DIR)\subdir v1db      $(MAKE) "BR_BASE_TYPE=FIXED" $@
#    +$(BR_MAKE_DIR)\subdir math      $(MAKE) "BR_BASE_TYPE=FIXED" $@
#    +$(BR_MAKE_DIR)\subdir fmt       $(MAKE) "BR_BASE_TYPE=FIXED" $@
