# $NetBSD: Makefile,v 1.58 2017/02/12 06:26:00 ryoon Exp $
#

DISTNAME=		gtk-send-pr-0.4.9
PKGREVISION=		29
CATEGORIES=		sysutils
MASTER_SITES=		http://download.berlios.de/gtk-send-pr/
EXTRACT_SUFX=		.tar.bz2

MAINTAINER=		mmendez@energyhq.be
HOMEPAGE=		http://gtk-send-pr.berlios.de/index.html
COMMENT=		GTK+ based problem report tool

USE_TOOLS+=		pkg-config

CPPFLAGS.SunOS+=	-Dstrsep=strpbrk
CPPFLAGS.IRIX+=		-Dstrsep=strpbrk
LDFLAGS.IRIX+=		-lgen

INSTALLATION_DIRS+=	bin ${PKGMANDIR}/man1
INSTALL_MAKE_FLAGS+=	PREFIX=${DESTDIR}${PREFIX}

.include "../../mail/libesmtp/buildlink3.mk"
.include "../../x11/gtk2/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
