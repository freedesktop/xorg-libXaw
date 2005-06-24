if BUILD_XAW6

lib_LTLIBRARIES = libXaw6.la

AM_CFLAGS =				\
        -I${top_srcdir}/include		\
        -I${top_srcdir}/include/X11/Xaw \
	$(XAW6_CFLAGS)

libXaw6_la_SOURCES = \
	$(top_srcdir)/src/Actions.c \
	$(top_srcdir)/src/AllWidgets.c \
	$(top_srcdir)/src/AsciiSink.c \
	$(top_srcdir)/src/AsciiSrc.c \
	$(top_srcdir)/src/AsciiText.c \
	$(top_srcdir)/src/Box.c \
	$(top_srcdir)/src/Command.c \
	$(top_srcdir)/src/Converters.c \
	$(top_srcdir)/src/Dialog.c \
	$(top_srcdir)/src/DisplayList.c \
	$(top_srcdir)/src/Form.c \
	$(top_srcdir)/src/Grip.c \
	$(top_srcdir)/src/Label.c \
	$(top_srcdir)/src/List.c \
	$(top_srcdir)/src/MenuButton.c \
	$(top_srcdir)/src/MultiSrc.c \
	$(top_srcdir)/src/MultiSink.c \
	$(top_srcdir)/src/OS.c \
	$(top_srcdir)/src/Paned.c \
	$(top_srcdir)/src/Panner.c \
	$(top_srcdir)/src/Pixmap.c \
	$(top_srcdir)/src/Porthole.c \
	$(top_srcdir)/src/PrintShell.c \
	$(top_srcdir)/src/Private.h \
	$(top_srcdir)/src/Repeater.c \
	$(top_srcdir)/src/Scrollbar.c \
	$(top_srcdir)/src/Simple.c \
	$(top_srcdir)/src/SimpleMenu.c \
	$(top_srcdir)/src/Sme.c \
	$(top_srcdir)/src/SmeBSB.c \
	$(top_srcdir)/src/SmeLine.c \
	$(top_srcdir)/src/StripChart.c \
	$(top_srcdir)/src/Text.c \
	$(top_srcdir)/src/TextSink.c \
	$(top_srcdir)/src/TextSrc.c \
	$(top_srcdir)/src/TextAction.c \
	$(top_srcdir)/src/TextPop.c \
	$(top_srcdir)/src/TextTr.c \
	$(top_srcdir)/src/Tip.c \
	$(top_srcdir)/src/Toggle.c \
	$(top_srcdir)/src/Tree.c \
	$(top_srcdir)/src/Vendor.c \
	$(top_srcdir)/src/Viewport.c \
	$(top_srcdir)/src/XawIm.c \
	$(top_srcdir)/src/XawInit.c \
	$(top_srcdir)/src/XawI18n.c \
	$(top_srcdir)/src/XawI18n.h \
	$(top_srcdir)/src/sharedlib.c

libXaw6_la_LDFLAGS = -version-info 6:1:0
libXaw6_la_LIBADD = $(XAW6_LIBS)

endif
