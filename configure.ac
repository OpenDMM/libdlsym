#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_INIT([libdlsym], [0.0.1], [enigma2-devel@lists.elitedvb.net])
AM_INIT_AUTOMAKE([dist-bzip2 foreign no-define tar-pax -Wno-portability])
AC_CONFIG_SRCDIR([src/symbol.c])
AC_CONFIG_HEADERS([libdlsym-config.h])

# Silent rules are available since 1.11, but older versions
# are still in use. So don't use them unconditionally.
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

AC_USE_SYSTEM_EXTENSIONS
AC_SYS_LARGEFILE

m4_ifdef([LT_INIT], [LT_INIT], [AC_PROG_LIBTOOL])
AC_CONFIG_MACRO_DIR([m4])

# Checks for programs.
AC_PROG_CC

# Checks for libraries.
AC_SEARCH_LIBS([dlopen], [dl])
AX_PTHREAD

# Checks for header files.
AC_CHECK_HEADERS([fcntl.h limits.h stdlib.h string.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_OFF_T
AC_TYPE_SIZE_T
AC_TYPE_SSIZE_T

AC_CONFIG_FILES([
	Makefile
	src/Makefile
	libdlsym.pc
])
AC_OUTPUT
