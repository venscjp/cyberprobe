
bin_PROGRAMS = cyberprobe cybermon nhis11-rcvr etsi-rcvr cyberprobe-cli

cyberprobe_SOURCES = cyberprobe.C nhis11.C sender.C \
	delivery.C xml.C capture.C configuration.C control.C snort_alert.C \
	sender.h delivery.h capture.h \
	configuration.h control.h snort_alert.h target.h \
	parameters.h packet_consumer.h interface.h \
	endpoint.h parameter.h
cyberprobe_LDADD = libcybermon.la -lssl

cybermon_SOURCES = cybermon.C management.h 
cybermon_LDADD = libcybermon.la -lssl

cyberprobe_cli_SOURCES = cyberprobe-cli.C readline.C readline.h
cyberprobe_cli_LDADD = libcybermon.la -lssl

nhis11_rcvr_SOURCES = nhis11_rcvr.C nhis11.C
nhis11_rcvr_LDADD = libcybermon.la -lssl

etsi_rcvr_SOURCES = etsi_rcvr.C
etsi_rcvr_LDADD = libcybermon.la -lssl

lib_LTLIBRARIES = libcybermon.la

libcybermon_la_SOURCES = address.C base_context.C ber.C			\
	cybermon-lua.C dns_over_tcp.C dns_over_udp.C dns_protocol.C	\
	engine.C etsi_li.C forgery.C ftp.C http.C icmp.C imap.C		\
	imap_ssl.C ip.C ntp.C ntp_protocol.C pop3.C pop3_ssl.C		\
	reaper.C resource_manager.C rtp.C rtp_ssl.C sip.C sip_context.C \
	sip_ssl.C	\
	smtp.C smtp_auth.C socket.C tcp.C tcp_ports.C udp.C udp_ports.C unrecognised.C		\
	../include/cybermon/address.h ../include/cybermon/ber.h		\
	../include/cybermon/base_context.h				\
	../include/cybermon/context.h					\
	../include/cybermon/cybermon-lua.h				\
	../include/cybermon/dns_context.h				\
	../include/cybermon/dns_over_tcp.h				\
	../include/cybermon/dns_over_udp.h				\
	../include/cybermon/dns_protocol.h				\
	../include/cybermon/engine.h ../include/cybermon/etsi_li.h	\
	../include/cybermon/exception.h ../include/cybermon/forgery.h	\
	../include/cybermon/flow.h ../include/cybermon/ftp.h		\
	../include/cybermon/http.h ../include/cybermon/icmp.h		\
	../include/cybermon/imap.h ../include/cybermon/imap_context.h	\
	../include/cybermon/imap_ssl.h					\
	../include/cybermon/imap_ssl_context.h				\
	../include/cybermon/ip.h ../include/cybermon/manager.h		\
	../include/cybermon/monitor.h ../include/cybermon/nhis11.h	\
	../include/cybermon/ntp.h ../include/cybermon/ntp_protocol.h	\
	../include/cybermon/observer.h					\
	../include/cybermon/packet_capture.h				\
	../include/cybermon/pdu.h ../include/cybermon/pop3.h		\
	../include/cybermon/pop3_context.h				\
	../include/cybermon/pop3_ssl.h					\
	../include/cybermon/pop3_ssl_context.h				\
	../include/cybermon/protocol.h ../include/cybermon/reaper.h	\
	../include/cybermon/resource.h ../include/cybermon/rtp.h	\
	../include/cybermon/rtp_context.h				\
	../include/cybermon/rtp_ssl.h ../include/cybermon/serial.h	\
	../include/cybermon/sip.h ../include/cybermon/sip_context.h	\
	../include/cybermon/sip_ssl.h ../include/cybermon/smtp.h	\
	../include/cybermon/smtp_auth.h					\
	../include/cybermon/smtp_auth_context.h				\
	../include/cybermon/socket.h					\
	../include/cybermon/specification.h ../include/cybermon/tcp.h	\
	../include/cybermon/thread.h ../include/cybermon/transport.h	\
	../include/cybermon/udp.h ../include/cybermon/unrecognised.h	\
	../include/cybermon/xml.h

ACLOCAL_AMFLAGS = -I m4

AM_CPPFLAGS = -I$(top_srcdir)/include
AM_LDFLAGS = 

LDFLAGS_BOOST = \
    $(BOOST_REGEX_LDFLAGS) $(BOOST_PROGRAM_OPTIONS_LDFLAGS)

LIBS_BOOST = \
    $(BOOST_REGEX_LIBS) $(BOOST_PROGRAM_OPTIONS_LIBS)

AM_CPPFLAGS += $(BOOST_CPPFLAGS) $(LUA_INCLUDE)
AM_LDFLAGS += $(LDFLAGS_BOOST) $(LUA_LDADD)
LIBS += $(LIBS_BOOST) $(LUA_LIB)

