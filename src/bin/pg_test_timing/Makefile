# src/bin/pg_test_timing/Makefile

PGFILEDESC = "pg_test_timing - test timing overhead"
PGAPPICON = win32

subdir = src/bin/pg_test_timing
top_builddir = ../../..
include $(top_builddir)/src/Makefile.global

OBJS = \
	$(WIN32RES) \
	pg_test_timing.o

all: pg_test_timing

pg_test_timing: $(OBJS) | submake-libpgport
	$(CC) $(CFLAGS) $^ $(LDFLAGS) $(LDFLAGS_EX) $(LIBS) -o $@$(X)

install: all installdirs
	$(INSTALL_PROGRAM) pg_test_timing$(X) '$(DESTDIR)$(bindir)/pg_test_timing$(X)'

installdirs:
	$(MKDIR_P) '$(DESTDIR)$(bindir)'

check:
	$(prove_check)

installcheck:
	$(prove_installcheck)

oracle-check:
	$(oracle_prove_check)

oracle-installcheck:
	$(oracle_prove_installcheck)

uninstall:
	rm -f '$(DESTDIR)$(bindir)/pg_test_timing$(X)'

clean distclean:
	rm -f pg_test_timing$(X) $(OBJS)
	rm -rf tmp_check
