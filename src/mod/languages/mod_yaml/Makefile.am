include $(top_srcdir)/build/modmake.rulesam
MODNAME=mod_yaml

if HAVE_YAML

mod_LTLIBRARIES = mod_yaml.la
mod_yaml_la_SOURCES  = mod_yaml.c
mod_yaml_la_CFLAGS   = $(AM_CFLAGS)
mod_yaml_la_CPPFLAGS = $(AM_CPPFLAGS) $(YAML_CFLAGS)
mod_yaml_la_LIBADD   = $(switch_builddir)/libfreeswitch.la $(YAML_LIBS)
mod_yaml_la_LDFLAGS  = -avoid-version -module -no-undefined -shared

else
install: error
all: error
error:
	$(error You must install libyaml-dev to build mod_yaml)
endif
