DISTCHECK_CONFIGURE_FLAGS = \
	  	--with-systemdsystemunitdir=$$dc_install_base/$(systemdsystemunitdir)

SUBDIRS = probes libfslabel . resource

EXTRA_DIST = CHANGELOG.txt DEVELOPERS.txt AUTHORS.txt README.txt LICENSE.txt

bin_PROGRAMS = istatd

istatd_SOURCES = \
	main.h main.cpp \
	conf.h conf.cpp \
	argument.h argument.cpp \
	switchboard.h switchboard.cpp \
	socket.h socket.cpp \
	socketset.h socketset.cpp \
	clientset.h clientset.cpp \
	isr.h isr.cpp \
	daemon.h daemon.cpp \
	stats.h stats.cpp \
	token.h token.cpp \
	utility.h utility.cpp \
	system.h

istatd_LDADD = probes/libprobes.a libfslabel/libfslabel.a

if HAVE_SYSTEMD
systemdsystemunit_DATA = \
			istatd.service
endif
