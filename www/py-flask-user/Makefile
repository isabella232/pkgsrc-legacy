# $NetBSD: Makefile,v 1.11 2017/01/12 11:58:23 rodent Exp $

DISTNAME=	Flask-User-0.6.11
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	python www
MASTER_SITES=	${MASTER_SITE_PYPI:=F/Flask-User/}
DIST_SUBDIR=	${PKGBASE:tl:S/${PYPKGPREFIX}/py/1}

MAINTAINER=	rodent@NetBSD.org
HOMEPAGE=	http://github.com/lingthio/Flask-User
COMMENT=	Customizable user account management for Flask
LICENSE=	2-clause-bsd

DEPENDS+=	${PYPKGPREFIX}-passlib-[0-9]*:../../security/py-passlib
DEPENDS+=	${PYPKGPREFIX}-py-bcrypt-[0-9]*:../../security/py-py-bcrypt
DEPENDS+=	${PYPKGPREFIX}-cryptodome-[0-9]*:../../security/py-cryptodome
DEPENDS+=	${PYPKGPREFIX}-flask-[0-9]*:../../www/py-flask
DEPENDS+=	${PYPKGPREFIX}-flask-babel-[0-9]*:../../www/py-flask-babel
DEPENDS+=	${PYPKGPREFIX}-flask-login-[0-9]*:../../www/py-flask-login
DEPENDS+=	${PYPKGPREFIX}-flask-mail-[0-9]*:../../www/py-flask-mail
DEPENDS+=	${PYPKGPREFIX}-flask-sqlalchemy-[0-9]*:../../www/py-flask-sqlalchemy
DEPENDS+=	${PYPKGPREFIX}-flask-wtf-[0-9]*:../../www/py-flask-wtf

USE_PKGLOCALEDIR=	yes
USE_LANGUAGES=		# none

post-install:
	${CHMOD} -x ${DESTDIR}${PREFIX}/${PYSITELIB}/flask_user/translations/zh/LC_MESSAGES/flask_user.mo

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
