# $NetBSD: Makefile,v 1.1 2016/07/18 15:03:05 fhajny Exp $
#

.include "../../mail/dovecot2/Makefile.plugin"

PKGNAME=		${DISTNAME:S/dovecot/dovecot-ldap/}
COMMENT+=		(LDAP plugin)

CONFIGURE_ARGS+=	--with-ldap=plugin

INSTALLATION_DIRS+=	include/dovecot \
			lib/dovecot/auth lib/dovecot/dict

do-install:
	cd ${WRKSRC} && (\
		${LIBTOOL} --mode=install ${INSTALL_LIB} \
			src/auth/libauthdb_ldap.la \
			${DESTDIR}${PREFIX}/lib/dovecot/auth; \
		${LIBTOOL} --mode=install ${INSTALL_LIB} \
			src/lib-ldap/libdovecot-ldap.la \
			${DESTDIR}${PREFIX}/lib/dovecot; \
		${LIBTOOL} --mode=install ${INSTALL_LIB} \
			src/plugins/dict-ldap/libdict_ldap.la \
			${DESTDIR}${PREFIX}/lib/dovecot/dict; \
	)
	${INSTALL_DATA} ${WRKSRC}/src/lib-ldap/ldap-client.h \
		${DESTDIR}${PREFIX}/include/dovecot

.include "../../databases/openldap-client/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
