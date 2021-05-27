=================
x265 HEVC Encoder
=================

(copy from bitbucket)
-----------------------------

`x265 <https://www.videolan.org/developers/x265.html>`_ is an open
source HEVC encoder. See the developer wiki for instructions for
downloading and building the source.

x265 is free to use under the `GNU GPL <http://www.gnu.org/licenses/gpl-2.0.html>`_ 
and is also available under a commercial `license <http://x265.org>`_ 

------------------------------------------------------------------

Documentation : `<http://x265.readthedocs.org/en/master/>`_

Wiki : `<http://bitbucket.org/multicoreware/x265_git/wiki/>`_

Releases : `<https://bitbucket.org/multicoreware/x265_git/downloads/>`_
or `<http://ftp.videolan.org/pub/videolan/x265/>`_

Mailing List : `x265-devel@videolan.org <http://mailman.videolan.org/listinfo/x265-devel>`_

Report an issue : `<https://bitbucket.org/multicoreware/x265_git/issues?status=new&status=open>`_

---------------------------------------------------------

#x265 on freenode.irc.net (status unknown - maybe hijacked after freenode takeover?)

#x265 on libera.chat (status unknown - no activity, not registered)

#x265 on oftc.net

---------------------------------------------------------

for the impatient on linux:

# cd x265/build/linux
# ./make-Makefiles.bash
# make

Please note, that I had no success in building it with my cmake parameters with gcc (10.2.0), but instead used clang (11.1.0).

Furthermore I fixed some compiler warnings, which let it now build without any warning (at least on my machine with my chosen configuration parameters); they were of a relative mild nature and are NOT (I repeat: NOT) tested by me in any way. There may be side-effects or maybe they introduced bugs, which are not covered by simple compiler warnings/errors to the user.. so, if you choose to clone this repo, do it at your OWN risk!
