# $NetBSD: Makefile,v 1.21 2017/01/19 18:52:22 agc Exp $
#

DISTNAME=	xpdf-cyrillic-2011-aug-15
PKGNAME=	xpdf-cyrillic-20110815
CATEGORIES=	print
MASTER_SITES=	ftp://ftp.foolabs.com/pub/xpdf/
MASTER_SITES+=	http://gd.tuwien.ac.at/publishing/xpdf/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.foolabs.com/xpdf/
COMMENT=	Xpdf support files for Cyrillic
LICENSE=	gnu-gpl-v2 OR gnu-gpl-v3

DEPENDS+=	xpdf>=2.02:../../print/xpdf

WRKSRC=		${WRKDIR}/xpdf-cyrillic
NO_CONFIGURE=	yes
NO_BUILD=	yes

INSTALLATION_DIRS+=	share/xpdf/cyrillic

post-patch:
	${MV} ${WRKSRC}/add-to-xpdfrc ${WRKSRC}/add-to-xpdfrc.orig
	${SED} -e 's:/usr/local:'${PREFIX}':g' < ${WRKSRC}/add-to-xpdfrc.orig > ${WRKSRC}/add-to-xpdfrc

do-install:
	${INSTALL_DATA} ${WRKSRC}/Bulgarian.nameToUnicode \
	    ${WRKSRC}/KOI8-R.unicodeMap ${WRKSRC}/add-to-xpdfrc \
	    ${DESTDIR}${PREFIX}/share/xpdf/cyrillic

.include "../../mk/bsd.pkg.mk"
