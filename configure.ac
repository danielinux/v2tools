#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.68])
AC_INIT([xordiff], [0.1], [info@v2.cs.unibo.it])
AM_INIT_AUTOMAKE([foreign dist-bzip2])
AC_CONFIG_SRCDIR([xordiff.c])
AC_CONFIG_HEADERS([config.h])

# Checks for programs.
AC_PROG_CC

# Checks for libraries.
AC_CHECK_LIB([bz2], [BZ2_bzopen], , AC_MSG_ERROR("cannot find bz2 library."))
AC_CHECK_LIB([mhash], [mhash_init], , AC_MSG_ERROR("cannot find mhash library."))
AC_CHECK_LIB([z], [gzopen], , AC_MSG_ERROR("cannot find z library."))

# Checks for header files.
AC_CHECK_HEADERS([fcntl.h stdlib.h string.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_C_INLINE
AC_TYPE_OFF_T
AC_TYPE_SIZE_T
AC_TYPE_SSIZE_T
AC_CHECK_MEMBERS([struct stat.st_blksize])

# Checks for library functions.
AC_CHECK_FUNCS([ftruncate memset])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
