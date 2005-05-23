dnl Process this file with autoconf to create configure.

AC_PREREQ([2.57])

AC_INIT([libXaw],
	7.0.2,
	[reed@reedmedia.net],
	libXaw)

AM_INIT_AUTOMAKE([dist-bzip2])

AM_CONFIG_HEADER(config.h)

# Check for progs
AC_PROG_CC
AC_PROG_LIBTOOL


# Whether to build Xaw6

AC_ARG_ENABLE(xaw6, AC_HELP_STRING([--disable-xaw6],
				[Disable building of libXaw.so.6]),
			[build_v6=$enableval], [build_v6=yes])

if test "x$build_v6" = xyes; then
   PKG_CHECK_MODULES(XAW6, xproto x11 xt xmu xpm)

   AC_SUBST(XAW6_CFLAGS)
   AC_SUBST(XAW6_LIBS)
fi


# Whether to build Xaw7

AC_ARG_ENABLE(xaw7, AC_HELP_STRING([--disable-xaw7],
				[Disable building of libXaw.so.7]),
			[build_v7=$enableval], [build_v7=yes])

if test "x$build_v7" = xyes; then
   PKG_CHECK_MODULES(XAW7, xproto x11 xt xmu xpm)

   AC_SUBST(XAW7_CFLAGS)
   AC_SUBST(XAW7_LIBS)
fi


# Whether to build Xaw8

AC_ARG_ENABLE(xaw8, AC_HELP_STRING([--disable-xaw8],
				[Disable building of libXaw.so.8]),
			[build_v8=$enableval], [build_v8=yes])

if test "x$build_v8" = xyes; then
   PKG_CHECK_MODULES(XPRINT, xp, xprint_found=yes, xprint_found=no)

   if test x$xprint_found = xno ; then
      AC_ERROR([
	Xprint is required to build libXaw.so.8. You can disable
	building of libXaw.so.8 by passing --disable-xaw8 to
	configure])
   fi

   PKG_CHECK_MODULES(XAW8, xproto x11 xt xmu xpm xp)

   AC_SUBST(XAW8_CFLAGS)
   AC_SUBST(XAW8_LIBS)
fi

AM_CONDITIONAL(BUILD_XAW6, [test x$build_v6 = xyes])
AM_CONDITIONAL(BUILD_XAW7, [test x$build_v7 = xyes])
AM_CONDITIONAL(BUILD_XAW8, [test x$build_v8 = xyes])

# Checks for header files.
AC_HEADER_STDC

AC_OUTPUT([Makefile
	  include/Makefile
	  man/Makefile
	  Xaw6/Makefile
	  Xaw7/Makefile
	  Xaw8/Makefile])

if test "x$build_v6" = xyes; then
   AC_OUTPUT(xaw6.pc)
fi

if test "x$build_v7" = xyes; then
   AC_OUTPUT(xaw7.pc)
fi

if test "x$build_v8" = xyes; then
   AC_OUTPUT(xaw8.pc)
fi
