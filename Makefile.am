SUBDIRS = include Xaw6 Xaw7 Xaw8 man

pkgconfigdir = $(libdir)/pkgconfig

pkgconfig_DATA = 

if BUILD_XAW6

pkgconfig_DATA += xaw6.pc

endif

if BUILD_XAW7

pkgconfig_DATA += xaw7.pc

endif

if BUILD_XAW8

pkgconfig_DATA += xaw8.pc

endif

EXTRA_DIST = $(man3_MANS) xaw6.pc.in xaw7.pc.in xaw8.pc.in autogen.sh
