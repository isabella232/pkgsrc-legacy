# $NetBSD: Makefile,v 1.9 2016/03/05 11:28:23 jperkin Exp $

DISTNAME=	apache-log4cxx-0.10.0
PKGNAME=	${DISTNAME:S/apache-//}
PKGREVISION=	6
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_APACHE:=logging/log4cxx/0.10.0/}

MAINTAINER=	reed@reedmedia.net
HOMEPAGE=	http://logging.apache.org/log4cxx/
COMMENT=	Logging framework for C++

GNU_CONFIGURE=	yes
USE_LIBTOOL=	yes
USE_TOOLS+=	gmake pkg-config
# c for configure
USE_LANGUAGES=	c c++

CONFIGURE_ARGS+=	--disable-doxygen --disable-html-docs

PKGCONFIG_OVERRIDE+=	liblog4cxx.pc.in

.include "../../devel/apr/buildlink3.mk"
.include "../../devel/apr-util/buildlink3.mk"

.include "../../mk/bsd.pkg.mk"
