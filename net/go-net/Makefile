# $NetBSD: Makefile,v 1.16 2017/04/13 15:12:05 bsiegert Exp $

DISTNAME=		go-net-20170308
PKGREVISION=		1
CATEGORIES=		net
MASTER_SITES=		${MASTER_SITE_GITHUB:=golang/}
GITHUB_PROJECT=		net
GITHUB_TAG=		a6577fa

MAINTAINER=		bsiegert@NetBSD.org
HOMEPAGE=		http://golang.org/
COMMENT=		Supplementary network libraries for Go
LICENSE=		modified-bsd

GO_SRCPATH=		golang.org/x/net
GO_DIST_BASE=		${GITHUB_PROJECT}-${GITHUB_TAG}*

.include "../../mk/bsd.prefs.mk"

PLIST_VARS+=	notsunos

.if ${OPSYS} != "SunOS"
# route support is not yet implemented for sunos
# h2i is missing terminal.MakeRaw and terminal.Restore
PLIST.notsunos=	yes
.endif

.include "../../textproc/go-text/buildlink3.mk"
.include "../../security/go-crypto/buildlink3.mk"
.include "../../lang/go/go-package.mk"
.include "../../mk/bsd.pkg.mk"
