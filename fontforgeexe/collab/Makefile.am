# Copyright (C) 2000-2012 by George Williams
# Copyright (C) 2013 by Ben Martin
#
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions are met:
#
# Redistributions of source code must retain the above copyright notice, this
# list of conditions and the following disclaimer.
#
# Redistributions in binary form must reproduce the above copyright notice,
# this list of conditions and the following disclaimer in the documentation
# and/or other materials provided with the distribution.
#
# The name of the author may not be used to endorse or promote products
# derived from this software without specific prior written permission.
#
# THIS SOFTWARE IS PROVIDED BY THE AUTHOR ``AS IS'' AND ANY EXPRESS OR IMPLIED
# WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
# MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
# EVENT SHALL THE AUTHOR BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
# SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
# PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
# OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
# WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
# OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
# ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

include $(top_srcdir)/mk/layout.am

#--------------------------------------------------------------------------


noinst_HEADERS = fontforge-internal-collab-server.h
EXTRA_DIST = 
MOSTLYCLEANFILES =

#--------------------------------------------------------------------------

if LIBZMQ

internal_bin_PROGRAMS = fontforge-internal-collab-server

fontforge_internal_collab_server_SOURCES = fontforge-internal-collab-server.c
fontforge_internal_collab_server_CPPFLAGS = $(AM_CPPFLAGS) \
  "-I$(top_builddir)/inc" \
  "-I$(top_srcdir)/inc" \
  $(MY_CFLAGS) $(LIBZMQ_CFLAGS)
fontforge_internal_collab_server_LDADD = $(LDADD) \
   $(top_builddir)/collab/libzmqcollab.la \
   $(top_builddir)/gutils/libgutils.la \
   $(top_builddir)/Unicode/libgunicode.la
fontforge_internal_collab_server_LDFLAGS = $(MY_CFLAGS) $(MY_LIBS) $(LIBZMQ_LIBS) -export-dynamic

endif

#--------------------------------------------------------------------------

-include $(top_srcdir)/git.mk
