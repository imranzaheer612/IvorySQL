# src/oracle_test/modules/injection_points/Makefile

MODULES = injection_points

EXTENSION = injection_points
DATA = injection_points--1.0.sql
PGFILEDESC = "injection_points - facility for injection points"

REGRESS = injection_points

ifdef USE_PGXS
PG_CONFIG = pg_config
PGXS := $(shell $(PG_CONFIG) --pgxs)
include $(PGXS)
else
subdir = src/oracle_test/modules/injection_points
top_builddir = ../../../..
include $(top_builddir)/src/Makefile.global
include $(top_srcdir)/contrib/contrib-global.mk
endif
