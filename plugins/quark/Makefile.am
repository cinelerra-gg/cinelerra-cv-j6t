plugin_LTLIBRARIES = quark.la
quark_la_LDFLAGS = -avoid-version -module -shared
quark_la_LIBADD =
quark_la_SOURCES = quark.C quarkwindow.C
AM_CFLAGS =
AM_CXXFLAGS =

AM_CPPFLAGS = -I$(top_srcdir)/guicast -I$(top_srcdir)/cinelerra -I$(top_srcdir)/quicktime
LIBTOOL = $(SHELL) $(top_builddir)/libtool $(LTCXX_FLAGS)

noinst_HEADERS = quark.h quarkwindow.h 
EXTRA_DIST = picon.png

quark.o: picon_png.h
picon_png.h: picon.png
	$(top_builddir)/guicast/pngtoh $^ > $@ || { rm -f $@; exit 1; }
clean-local:
	$(RM) picon_png.h
