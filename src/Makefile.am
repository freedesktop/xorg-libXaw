lib_LTLIBRARIES =

#
# This doesn't appear to be used on any
# current systems -- it requires SUNSHLIB and !SHAREDCODE,
# but only sunLib.rules defines SUNSHLIB and that file also
# always defines SHAREDCODE. Go figure
#
# SHAREDLIB_SOURCES = sharedlib.c

COMMON_SOURCES = \
	Actions.c \
	AllWidgets.c \
	AsciiSink.c \
	AsciiSrc.c \
	AsciiText.c \
	Box.c \
	Command.c \
	Converters.c \
	Dialog.c \
	DisplayList.c \
	Form.c \
	Grip.c \
	Label.c \
	List.c \
	MenuButton.c \
	MultiSrc.c \
	MultiSink.c \
	OS.c \
	Paned.c \
	Panner.c \
	Pixmap.c \
	Porthole.c \
	Private.h \
	Repeater.c \
	Scrollbar.c \
	Simple.c \
	SimpleMenu.c \
	Sme.c \
	SmeBSB.c \
	SmeLine.c \
	StripChart.c \
	Text.c \
	TextSink.c \
	TextSrc.c \
	TextAction.c \
	TextPop.c \
	TextTr.c \
	Toggle.c \
	Tree.c \
	Vendor.c \
	Viewport.c \
	XawIm.c \
	XawInit.c \
	XawI18n.c \
	XawI18n.h

if BUILD_XAW6

lib_LTLIBRARIES += libXaw6.la

libXaw6_la_CFLAGS =			\
        -I${top_srcdir}/include		\
        -I${top_srcdir}/include/X11/Xaw \
	-DOLDXAW			\
	$(XAW6_CFLAGS)

libXaw6_la_SOURCES = \
	$(COMMON_SOURCES)

libXaw6_la_LDFLAGS = -version-info 6:1:0
libXaw6_la_LIBADD = $(XAW6_LIBS)

endif

if BUILD_XAW7

lib_LTLIBRARIES += libXaw7.la

libXaw7_la_CFLAGS =			\
        -I${top_srcdir}/include		\
        -I${top_srcdir}/include/X11/Xaw \
	-DXAW7				\
	$(XAW7_CFLAGS)

libXaw7_la_SOURCES = \
	$(COMMON_SOURCES) \
	Tip.c

libXaw7_la_LDFLAGS = -version-info 7:0:0
libXaw7_la_LIBADD = $(XAW7_LIBS)

endif

if BUILD_XAW8

lib_LTLIBRARIES += libXaw8.la

libXaw8_la_CFLAGS =			\
        -I${top_srcdir}/include		\
        -I${top_srcdir}/include/X11/Xaw \
	$(XAW8_CFLAGS)

libXaw8_la_SOURCES = \
	$(COMMON_SOURCES) \
	PrintShell.c \
	Tip.c

libXaw8_la_LDFLAGS = -version-info 8:0:0
libXaw8_la_LIBADD = $(XAW8_LIBS)

endif

EXTRA_DIST = sharedlib.c
