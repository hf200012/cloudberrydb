# contrib/pg_buffercache/Makefile

MODULE_big = pg_buffercache
OBJS = \
	$(WIN32RES) \
	pg_buffercache_pages.o

EXTENSION = pg_buffercache
DATA = pg_buffercache--1.2.sql pg_buffercache--1.2--1.3.sql \
	pg_buffercache--1.1--1.2.sql pg_buffercache--1.0--1.1.sql \
	pg_buffercache--1.3--1.4.sql \
	pg_buffercache--1.4--1.4.1.sql

PGFILEDESC = "pg_buffercache - monitoring of shared buffer cache in real-time"

REGRESS = pg_buffercache
REGRESS_OPTS += --init-file=$(top_srcdir)/src/test/regress/init_file

ifdef USE_PGXS
PG_CONFIG = pg_config
PGXS := $(shell $(PG_CONFIG) --pgxs)
include $(PGXS)
else
subdir = contrib/pg_buffercache
top_builddir = ../..
include $(top_builddir)/src/Makefile.global
include $(top_srcdir)/contrib/contrib-global.mk
endif
