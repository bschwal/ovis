lib_LTLIBRARIES =

AM_CFLAGS = $(DBGFLAGS) -I$(top_srcdir) -I.. @OVIS_LIB_INCDIR_FLAG@
AM_CPPFLAGS = -DSYSCONFDIR='"$(sysconfdir)"' -DPLUGINDIR='"$(pkglibdir)"'
AM_CFLAGS += \
"-DLDMS_SRCDIR=\"$(abs_top_srcdir)\"" \
"-DLDMS_BUILDDIR=\"$(abs_top_builddir)\""

ldmscoreincludedir = $(includedir)/ldms
ldmscoreinclude_HEADERS = ldms.h ldms_core.h ldms_xprt.h ldms_auth.h \
			  kldms_req.h ref.h

libldms_la_SOURCES = ldms.c ldms_xprt.c ldms_private.h \
		     ldms_auth.c ldms_xprt_auth.c \
		     ref.h
libldms_la_LIBADD = -ldl -lpthread -lcoll -ljson_util \
	@OVIS_LIB_LIB64DIR_FLAG@ @OVIS_LIB_LIBDIR_FLAG@ \
	-lmmalloc -lzap

lib_LTLIBRARIES += libldms.la

install-data-hook:
#	cp $(top_builddir)/scripts/ldmsd /etc/init.d/ldmsd
#	cp $(top_builddir)/scripts/schedstatd /etc/init.d/schedstatd
#	cp $(top_builddir)/scripts/meminfod /etc/init.d/meminfod
#	cp $(top_builddir)/scripts/sysclassibd /etc/init.d/sysclassibd
