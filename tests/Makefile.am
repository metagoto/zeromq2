INCLUDES = -I$(top_builddir)/include
LDADD = $(top_builddir)/src/libzmq.la

noinst_PROGRAMS = test_pair_inproc \
                  test_pair_ipc \
                  test_pair_tcp \
                  test_reqrep_inproc \
                  test_reqrep_ipc \
                  test_reqrep_tcp

if !ON_MINGW
noinst_PROGRAMS += test_shutdown_stress
endif

test_pair_inproc_SOURCES = test_pair_inproc.cpp testutil.hpp
test_pair_ipc_SOURCES = test_pair_ipc.cpp testutil.hpp
test_pair_tcp_SOURCES = test_pair_tcp.cpp testutil.hpp

test_reqrep_inproc_SOURCES = test_reqrep_inproc.cpp testutil.hpp
test_reqrep_ipc_SOURCES = test_reqrep_ipc.cpp testutil.hpp
test_reqrep_tcp_SOURCES = test_reqrep_tcp.cpp testutil.hpp

if !ON_MINGW
test_shutdown_stress_SOURCES = test_shutdown_stress.cpp
endif

TESTS = $(noinst_PROGRAMS)
