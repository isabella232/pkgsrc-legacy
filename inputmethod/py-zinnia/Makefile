# $NetBSD: Makefile,v 1.8 2017/01/01 14:43:44 wiz Exp $

.include "../../inputmethod/zinnia/Makefile.common"

PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES+=	python

COMMENT=	Zinnia python module

USE_TOOLS+=	pkg-config
USE_LANGUAGES=	c c++

PYSETUPSUBDIR=	python
PYTHON_VERSIONS_INCOMPATIBLE=	34 35 36 # not yet ported as of 0.06

EGG_NAME=	zinnia_python-0.0.0

BUILDLINK_API_DEPENDS.zinnia+=	zinnia>=${PKGVERSION_NOREV}
.include "../../inputmethod/zinnia/buildlink3.mk"
.include "../../lang/python/distutils.mk"
.include "../../mk/bsd.pkg.mk"
