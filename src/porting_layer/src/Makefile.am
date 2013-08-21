libporting_layer_la_CPPFLAGS = \
	-DLIBDIR=\"@libdir@\" \
	$(NULL)

libporting_layer_la_INCLUDES = \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)/include/internal \
	-I$(top_srcdir)/src/porting_layer/include \
	$(NULL)

noinst_LTLIBRARIES = libporting_layer.la

libporting_layer_la_SOURCES = \
	$(top_srcdir)/src/porting_layer/src/plat_mmap_posix.c \
	$(top_srcdir)/src/porting_layer/src/plat_mmap_windows.c \
	$(top_srcdir)/src/porting_layer/src/plat_path.c \
	$(NULL)
