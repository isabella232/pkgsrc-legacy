# $NetBSD: Makefile,v 1.2 2017/06/05 14:25:04 ryoon Exp $

DISTNAME=	DateTime-Incomplete-0.08
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	1
CATEGORIES=	time perl5
MASTER_SITES=	http://search.cpan.org/CPAN/authors/id/F/FG/FGLOCK/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/CPAN/authors/id/F/FG/FGLOCK/
COMMENT=	DateTime::Incomplete - An incomplete datetime, like January 5
LICENSE=	${PERL5_LICENSE}

# for make test
BUILD_DEPENDS+=	p5-DateTime-Set-[0-9]*:../../time/p5-DateTime-Set
BUILD_DEPENDS+=	p5-DateTime-Event-Recurrence-[0-9]*:../../time/p5-DateTime-Event-Recurrence

PERL5_PACKLIST= auto/DateTime/Incomplete/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
