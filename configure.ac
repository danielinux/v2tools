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
AC_CHECK_LIB([bz2], [BZ2_bzopen], , echo && echo "Error: Cannot find bz2 library." && exit 1)
AC_CHECK_LIB([mhash], [mhash_init], , echo && echo "Error: Cannot find mhash library." && exit 1)
AC_CHECK_LIB([z], [gzopen], , echo && echo "Error: Cannot find z library." && exit 1)

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
