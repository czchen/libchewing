include $(top_srcdir)/src/common
include $(top_srcdir)/src/porting_layer
include $(top_srcdir)/src/tools

libchewing_la_INCLUDES = \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)/include/internal \
	-I$(top_srcdir)/src/porting_layer/include \
	-DCHEWING_DATADIR=\"$(datadir)/chewing\" \
	$(NULL)

noinst_HEADERS += \
	$(top_srcdir)/src/private.h \
	$(NULL)

lib_LTLIBRARIES += libchewing.la

libchewing_la_SOURCES = \
	$(top_srcdir)/src/char.c \
	$(top_srcdir)/src/chewingio.c \
	$(top_srcdir)/src/chewingutil.c \
	$(top_srcdir)/src/choice.c \
	$(top_srcdir)/src/dict.c \
	$(top_srcdir)/src/hash.c \
	$(top_srcdir)/src/tree.c \
	$(top_srcdir)/src/userphrase.c \
	$(top_srcdir)/src/zuin.c \
	$(top_srcdir)/src/pinyin.c \
	$(top_srcdir)/src/mod_aux.c \
	$(NULL)

libchewing_la_LIBADD = \
	$(top_builddir)/libcommon.la \
	$(top_builddir)/libporting_layer.la \
	$(NULL)

libchewing_la_LDFLAGS = \
	-version-number $(LIBCHEWING_MAJOR):$(LIBCHEWING_MINOR):$(LIBCHEWING_REVISION) \
	-rpath $(libdir) \
	-no-undefined \
	-Wl,--no-undefined \
	-export-symbols-regex "^(chewing)_" \
	$(NULL)

libchewing_la: $(generated_header)
