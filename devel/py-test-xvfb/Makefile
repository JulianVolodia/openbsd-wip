# $OpenBSD: Makefile,v 1.8 2017/04/22 18:02:15 shadchin Exp $

COMMENT =		pytest plugin to run Xvfb for tests

MODPY_EGG_VERSION =	1.1.0
DISTNAME =		pytest-xvfb-${MODPY_EGG_VERSION}
PKGNAME =		${DISTNAME:S/py/py-/}
CATEGORIES =		devel

HOMEPAGE =		https://github.com/The-Compiler/pytest-xvfb

# MIT
PERMIT_PACKAGE_CDROM =	Yes

MODULES =		lang/python
RUN_DEPENDS+=		devel/py-test${MODPY_FLAVOR} \
			x11/py-virtualdisplay${MODPY_FLAVOR}

MODPY_PI =		Yes
MODPY_SETUPTOOLS =	Yes

FLAVORS =		python3
FLAVOR ?=

TEST_DEPENDS +=		${RUN_DEPENDS} \
			devel/py-test-xvfb${MODPY_FLAVOR}
do-test:
	@cd ${WRKSRC} && ${MODPY_BIN} -m pytest

.include <bsd.port.mk>
