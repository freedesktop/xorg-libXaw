SUBDIRS = include Xaw6 Xaw7 Xaw8 man

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = 

if BUILD_XAW6

pkgconfig_DATA += xaw6.pc
DEFAULT_LIB = libXaw6.so

endif

if BUILD_XAW7

pkgconfig_DATA += xaw7.pc
DEFAULT_LIB = libXaw7.so

endif

if BUILD_XAW8

pkgconfig_DATA += xaw8.pc
DEFAULT_LIB = libXaw8.so

endif

EXTRA_DIST = xaw6.pc.in xaw7.pc.in xaw8.pc.in autogen.sh

install-exec-hook:
	cd $(libdir) && rm -f libXaw.so && ln -s $(DEFAULT_LIB) libXaw.so
