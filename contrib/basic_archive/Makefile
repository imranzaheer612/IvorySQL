# contrib/basic_archive/Makefile

MODULES = basic_archive
PGFILEDESC = "basic_archive - basic archive module"

REGRESS = basic_archive
ORA_REGRESS = basic_archive
REGRESS_OPTS = --temp-config $(top_srcdir)/contrib/basic_archive/basic_archive.conf
ORACLE_REGRESS_OPTS = --temp-config $(top_srcdir)/contrib/basic_archive/basic_archive.conf

# Disabled because these tests require special configuration, which
# typical installcheck users do not have (e.g. buildfarm clients).
NO_INSTALLCHECK = 1

ifdef USE_PGXS
PG_CONFIG = pg_config
PGXS := $(shell $(PG_CONFIG) --pgxs)
include $(PGXS)
else
subdir = contrib/basic_archive
top_builddir = ../..
include $(top_builddir)/src/Makefile.global
include $(top_srcdir)/contrib/contrib-global.mk
endif
