# $NetBSD: Makefile,v 1.18 2016/10/09 17:49:39 ryoon Exp $

DISTNAME=	gdk-pixbuf-${PIXBUF2_VERSION}
PKGNAME=	gdk-pixbuf2-xlib-${PIXBUF2_VERSION}
CATEGORIES=	graphics
MASTER_SITES=	${MASTER_SITE_GNOME:=sources/gdk-pixbuf/${MSITE_VERSION}/}
EXTRACT_SUFX=	.tar.xz

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.gnome.org/
COMMENT=	Image loaders for gtk2
LICENSE=	gnu-gpl-v2

PATCHDIR=	${.CURDIR}/../../graphics/gdk-pixbuf2/patches
DISTINFO_FILE=	${.CURDIR}/../../graphics/gdk-pixbuf2/distinfo
BUILD_DIRS=	contrib/gdk-pixbuf-xlib
INSTALL_DIRS=	contrib/gdk-pixbuf-xlib

CONFLICTS+=	gtk2+<2.22

.include "../../graphics/gdk-pixbuf2/Makefile.version"

GNU_CONFIGURE=		yes
CONFIGURE_ARGS+=	--without-libtiff --without-libjpeg --without-libpng
CONFIGURE_ARGS+=	--with-x11
USE_LIBTOOL=		yes
USE_TOOLS+=		pkg-config
USE_PKGLOCALEDIR=	yes

PKGCONFIG_OVERRIDE+=	contrib/gdk-pixbuf-xlib/gdk-pixbuf-xlib-2.0.pc.in
PKGCONFIG_OVERRIDE+=	gdk-pixbuf-2.0.pc.in

.include "../../graphics/gdk-pixbuf2/buildlink3.mk"
BUILDLINK_API_DEPENDS.glib2+= glib2>=2.26.0
.include "../../devel/glib2/buildlink3.mk"
.include "../../x11/libX11/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
