include $(top_srcdir)/config/Rules.am

DEFAULT_INCLUDES += \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)/lib/libspl/include

sbin_PROGRAMS = zstreamdump

zstreamdump_SOURCES = \
	zstreamdump.c

zstreamdump_LDFLAGS = -Wl,--start-group \
	$(top_builddir)/lib/libzpool/libzpool.la \
	$(top_builddir)/lib/libnvpair/libnvpair.la \
	$(top_builddir)/lib/libuutil/libuutil.la \
	${UZFS_LIB}	\
	$(top_builddir)/lib/libzfs/libzfs.la \
	$(top_builddir)/lib/libzfs_core/libzfs_core.la -Wl,--end-group
