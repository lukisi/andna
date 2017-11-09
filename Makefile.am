NULL = 
ACLOCAL_AMFLAGS = -I m4
.PHONY: check

noinst_LTLIBRARIES = \
	libandna.la \
	$(NULL)

libandna_la_SOURCES = \
	andna.vala \
	serializables.vala \
	$(NULL)

libandna_la_VALAFLAGS = \
	-H andna.h \
	--library andna \
	--vapidir $(GEE_PREFIX)/share/vala/vapi \
	--vapidir $(JSON_PREFIX)/share/vala-0.32/vapi \
	--vapidir $(TASKLETSYSTEM_VAPIDIR) \
	--vapidir $(NTKDCOMMON_VAPIDIR) \
	--vapidir $(NTKDRPC_VAPIDIR) \
	--vapidir $(PEERS_VAPIDIR) \
	--pkg gee-0.8 \
	--pkg json-glib-1.0 \
	--pkg tasklet-system \
	--pkg ntkd-common \
	--pkg ntkdrpc\
	--pkg peers \
	$(NULL)

libandna_la_CPPFLAGS = \
	-w \
	$(GOBJECT_CFLAGS) \
	$(GEE_CFLAGS) \
	$(JSONGLIB_CFLAGS) \
	$(TASKLETSYSTEM_CFLAGS) \
	$(NTKDCOMMON_CFLAGS) \
	$(NTKDRPC_CFLAGS) \
	$(PEERS_CFLAGS) \
	$(NULL)

libandna_la_LIBADD = \
	$(GOBJECT_LIBS) \
	$(GEE_LIBS) \
	$(JSONGLIB_LIBS) \
	$(TASKLETSYSTEM_LIBS) \
	$(NTKDCOMMON_LIBS) \
	$(NTKDRPC_LIBS) \
	$(PEERS_LIBS) \
	$(NULL)

MAINTAINERCLEANFILES = \
	$(srcdir)/andna.vapi \
	$(NULL)

andna.vapi: libandna_la_vala.stamp
	$(NULL)

