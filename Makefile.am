SUBDIRS = gphoto-m4 contrib doc gphoto2 packaging po tests

ACLOCAL_AMFLAGS = -I auto-m4 -I gphoto-m4
EXTRA_DIST = README.md

README: $(srcdir)/README.md
	cp $(srcdir)/README.md README

@GP_GETTEXT_SETUP_MK@

# We need *some* `all-local` target (dummy or real) to force Automake
# to make the `all` target depend on it.  In this case, print build
# flags for debugging purposes.
all-local:
	@test -z "$(CFLAGS)"   || printf "  %s %-8s %s\n" env CFLAGS   "$(CFLAGS)"
	@test -z "$(CPPFLAGS)" || printf "  %s %-8s %s\n" env CPPFLAGS "$(CPPFLAGS)"
	@test -z "$(LDADD)"    || printf "  %s %-8s %s\n" env LDADD    "$(LDADD)"
	@test -z "$(LDFLAGS)"  || printf "  %s %-8s %s\n" env LDFLAGS  "$(LDFLAGS)"

# Dummy target to force Automake to make the "distclean" target depend on it
distclean-local:
	@:
