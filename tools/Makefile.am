## Makefile.am

AM_CPPFLAGS = ${libuuid_CFLAGS} -I$(top_srcdir)/include
AM_CFLAGS = -Wall
sbin_PROGRAMS = f2fstat
if !WINDOWS
sbin_PROGRAMS += fibmap.f2fs parse.f2fs
endif
f2fstat_SOURCES = f2fstat.c
fibmap_f2fs_SOURCES = fibmap.c
parse_f2fs_SOURCES = f2fs_io_parse.c

if LINUX
sbin_PROGRAMS += f2fscrypt
f2fscrypt_SOURCES = f2fscrypt.c sha512.c
f2fscrypt_LDFLAGS = ${libuuid_LIBS}
dist_man_MANS = f2fscrypt.8
endif

SUBDIRS = sg_write_buffer f2fs_io
