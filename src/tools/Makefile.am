sort_CC = $(CC_FOR_BUILD)

sort_CFLAGS = $(CFLAGS_FOR_BUILD)

sort_INCLUDES = \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)/include/internal \
	-I$(top_srcdir)/src \
	-I$(top_srcdir)/src/porting_layer/include \
	$(NULL)

sort_SOURCES = \
	$(top_srcdir)/src/tools/sort.c \
	$(top_srcdir)/src/common/key2pho.c \
	$(top_srcdir)/src/common/chewing-utf8-util.c \
	$(NULL)


maketree_CC = $(CC_FOR_BUILD)

maketree_CFLAGS = $(CFLAGS_FOR_BUILD)

maketree_INCLUDES = \
	-I$(top_srcdir)/include \
	-I$(top_srcdir)/include/internal \
	-I$(top_srcdir)/src \
	-I$(top_srcdir)/src/porting_layer/include \
	$(NULL)

maketree_SOURCES =
	$(top_srcdir)/src/tools/maketree.c \
	$(NULL)

noinst_PROGRAMS = sort maketree
