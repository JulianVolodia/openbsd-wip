# $OpenBSD: Makefile,v 1.58 2018/06/22 08:30:46 landry Exp $

COMMENT =	qt implementation of freedesktop.org xdg specs

VERSION =	3.2.0

NAME=		libqtxdg
DISTNAME =	${NAME}-${VERSION}

SHARED_LIBS +=  Qt5Xdg                    0.0 # 0.0
SHARED_LIBS +=  Qt5XdgIconLoader          0.0 # 0.0

WANTLIB +=	${COMPILER_LIBCXX} Qt5Core Qt5Gui Qt5Svg Qt5Widgets
WANTLIB +=	m Qt5DBus Qt5Xml

LIB_DEPENDS +=		x11/qt5/qtbase,-main \
			x11/qt5/qtsvg

BUILD_DEPENDS +=	x11/qt5/qttools


CONFIGURE_ARGS +=	-DBUILD_TESTS=Yes
CONFIGURE_ENV +=	Qt5_DIR=${LOCALBASE}/lib/qt5/cmake


.include <bsd.port.mk>
