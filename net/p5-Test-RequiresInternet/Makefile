# $NetBSD: Makefile,v 1.5 2017/06/05 14:24:25 ryoon Exp $

DISTNAME=	Test-RequiresInternet-0.05
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	2
CATEGORIES=	net
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Test/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/~mallen/Test-RequiresInternet/
COMMENT=	Test::RequiresInternet - Easily test network connectivity
LICENSE=	${PERL5_LICENSE}

PERL5_PACKLIST=	auto/Test/RequiresInternet/.packlist
USE_LANGUAGES=	# none

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
