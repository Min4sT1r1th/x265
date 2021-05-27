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

Please note, that I had no success in building it with my cmake parameters with gcc (10.2.0), but instead used clang (11.1.0) :

```
cmake \
-DCMAKE_INSTALL_PREFIX='/usr' \
-DCMAKE_INSTALL_BINDIR='/usr/bin' \
-DCMAKE_INSTALL_DATADIR='/usr/share' \
-DCMAKE_INSTALL_INCLUDEDIR='/usr/include' \
-DCMAKE_INSTALL_OLDINCLUDEDIR='/usr/include' \
-DCMAKE_INSTALL_DATAROOTDIR='/usr/share' \
-DCMAKE_INSTALL_LOCALEDIR='/usr/locale' \
-DCMAKE_INSTALL_INFODIR='/usr/share/info' \
-DCMAKE_INSTALL_LIBDIR='/usr/lib' \
-DCMAKE_INSTALL_LIBEXECDIR='/usr/libexec' \
-DCMAKE_INSTALL_LOCALSTATEDIR='/var' \
-DCMAKE_INSTALL_MANDIR='/usr/share/man' \
-DCMAKE_INSTALL_SBINDIR='/usr/sbin' \
-DCMAKE_INSTALL_SHAREDSTATEDIR='/var' \
-DCMAKE_INSTALL_SYSCONFDIR='/etc' \
-DCMAKE_ADDR2LINE='/usr/bin/addr2line' \
-DCMAKE_AR='/usr/bin/ar' \
-DCMAKE_ASM_NASM_COMPILER='/usr/bin/nasm' \
-DCMAKE_C_COMPILER='ccache-clang' \
-DCMAKE_C_COMPILER_AR='/usr/bin/gcc-ar' \
-DCMAKE_C_COMPILER_RANLIB='/usr/bin/gcc-ranlib' \
-DCMAKE_CXX_COMPILER='ccache-clang++' \
-DCMAKE_LINKER='/usr/bin/ld' \
-DCMAKE_MAKE_PROGRAM='/usr/bin/make' \
-DCMAKE_NM='/usr/bin/nm' \
-DCMAKE_OBJCOPY='/usr/bin/objcopy' \
-DCMAKE_OBJDUMP='/usr/bin/objdump' \
-DCMAKE_RANLIB='/usr/bin/ranlib' \
-DCMAKE_READELF='/usr/bin/readelf' \
-DCMAKE_STRIP='/usr/bin/strip' \
-DCMAKE_ASM_NASM_FLAGS='-w-macro-params-legacy' \
-DCMAKE_ASM_NASM_FLAGS_DEBUG='-g' \
-DCMAKE_ASM_NASM_FLAGS_MINSIZEREL='' \
-DCMAKE_ASM_NASM_FLAGS_RELEASE='' \
-DCMAKE_ASM_NASM_FLAGS_RELWITHDEBINFO='-g' \
-DCMAKE_C_FLAGS='-fstack-protector-strong -Wformat -Werror' \
-DCMAKE_C_FLAGS_DEBUG='-g' \
-DCMAKE_C_FLAGS_MINSIZEREL='-Os -DNDEBUG' \
-DCMAKE_C_FLAGS_RELEASE='-O3 -DNDEBUG' \
-DCMAKE_C_FLAGS_RELWITHDEBINFO='-O2 -g -DNDEBUG' \
-DCMAKE_EXE_LINKER_FLAGS='-L/usr/lib -lvmaf' \
-DCMAKE_EXE_LINKER_FLAGS_DEBUG='' \
-DCMAKE_EXE_LINKER_FLAGS_MINSIZEREL='' \
-DCMAKE_EXE_LINKER_FLAGS_RELEASE='' \
-DCMAKE_EXE_LINKER_FLAGS_RELWITHDEBINFO='' \
-DCMAKE_MODULE_LINKER_FLAGS='' \
-DCMAKE_MODULE_LINKER_FLAGS_DEBUG='' \
-DCMAKE_MODULE_LINKER_FLAGS_MINSIZEREL='' \
-DCMAKE_MODULE_LINKER_FLAGS_RELEASE='' \
-DCMAKE_MODULE_LINKER_FLAGS_RELWITHDEBINFO='' \
-DCMAKE_SHARED_LINKER_FLAGS='' \
-DCMAKE_SHARED_LINKER_FLAGS_DEBUG='' \
-DCMAKE_SHARED_LINKER_FLAGS_MINSIZEREL='' \
-DCMAKE_SHARED_LINKER_FLAGS_RELEASE='' \
-DCMAKE_SHARED_LINKER_FLAGS_RELWITHDEBINFO='' \
-DCMAKE_STATIC_LINKER_FLAGS='' \
-DCMAKE_STATIC_LINKER_FLAGS_DEBUG='' \
-DCMAKE_STATIC_LINKER_FLAGS_MINSIZEREL='' \
-DCMAKE_STATIC_LINKER_FLAGS_RELEASE='' \
-DCMAKE_STATIC_LINKER_FLAGS_RELWITHDEBINFO='' \
-DCMAKE_SKIP_INSTALL_RPATH='OFF' \
-DCMAKE_SKIP_RPATH='OFF' \
-DCMAKE_BUILD_TYPE='Release' \
-DCMAKE_COLOR_MAKEFILE='ON' \
-DCMAKE_EXPORT_COMPILE_COMMANDS='ON' \
-DCMAKE_VERBOSE_MAKEFILE='ON' \
-DCMAKE_CXX_FLAGS='-fstack-protector-strong -Wformat -Werror' \
-DBIN_INSTALL_DIR='bin' \
-DCHECKED_BUILD='OFF' \
-DDETAILED_CU_STATS='OFF' \
-DENABLE_AGGRESSIVE_CHECKS='ON' \
-DENABLE_ASSEMBLY='ON' \
-DENABLE_CLI='ON' \
-DENABLE_HDR10_PLUS='OFF' \
-DENABLE_LIBNUMA='ON' \
-DENABLE_LIBVMAF='ON' \
-DENABLE_PIC='ON' \
-DENABLE_PPA='OFF' \
-DENABLE_SHARED='ON' \
-DENABLE_SVT_HEVC='ON' \
-DENABLE_TESTS='ON' \
-DENABLE_VTUNE='OFF' \
-DHIGH_BIT_DEPTH='OFF' \
-DLIB_INSTALL_DIR='lib' \
-DNO_ATOMICS='OFF' \
-DSTATIC_LINK_CRT='OFF' \
-DWARNINGS_AS_ERRORS='OFF' \
../../source
```
