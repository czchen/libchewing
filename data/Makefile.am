if ENABLE_BINARY_DATA
chindexs = \
	$(top_srcdir)/ch_index_begin.dat \
	$(top_srcdir)/ch_index_phone.dat \
	$(NULL)
else
chindexs = \
	$(top_srcdir)/ch_index.dat \
	$(NULL)
endif

datas = \
	$(top_srcdir)/us_freq.dat \
	$(top_srcdir)/dict.dat \
	$(top_srcdir)/ph_index.dat \
	$(top_srcdir)/fonetree.dat \
	$(chindexs) \
	$(NULL)

static_tables = \
	$(top_srcdir)\pinyin.tab \
	$(top_srcdir)\swkb.dat \
	$(top_srcdir)\symbols.dat \
	$(NULL)

generated_header = \
	$(top_builddir)/src/chewing-definition.h \
	$(NULL)

dist_noinst_DATA = \
	$(top_srcdir)\NOTE \
	$(top_srcdir)\phone.cin \
	$(top_srcdir)\phone.cin-CNS11643-complete.patch \
	$(top_srcdir)\svnrev \
	$(top_srcdir)\tsi.src \
	$(NULL)

chewing_datadir = $(pkglibdir)
chewing_data_DATA = \
	$(static_tables) \
	$(datas) \
	$(NULL)

all: $(datas)

$(datas): gendata_stamp

gendata_stamp $(generated_header): phone.cin tsi.src $(tooldir)/sort$(EXEEXT) $(tooldir)/maketree$(EXEEXT)
	env LC_ALL=C $(top_builddir)/sort$(EXEEXT) $(top_srcdir)/data/phone.cin $(top_srcdir)/data/tsi.src
	$(top_builddir)/maketree$(EXEEXT)
	-rm -f phoneid.dic
	-mkdir -p $(top_builddir)/data
	-mv $(datas) $(top_builddir)/data
	-mv -f chewing-definition.h $(generated_header)
	touch $@

CLEANFILES += $(datas) gendata_stamp $(generated_header)
