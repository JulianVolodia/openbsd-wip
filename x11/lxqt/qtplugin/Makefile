# $OpenBSD$

COMMENT =	lxqt qt platform integration plugin

VERSION =	0.13.0

NAME=		lxqt-qtplugin
DISTNAME =	${NAME}-${VERSION}

WANTLIB += ${COMPILER_LIBCXX} Qt5Core Qt5DBus Qt5Gui Qt5Svg Qt5Widgets
WANTLIB += Qt5X11Extras Qt5XdgIconLoader dbusmenu-qt5 exif fm
WANTLIB += fm-qt gio-2.0 glib-2.0 gobject-2.0 gthread-2.0 intl
WANTLIB += m menu-cache xcb

LIB_DEPENDS +=		x11/qt5/qtx11extras \
			x11/lxqt/libqtxdg \
			x11/lxqt/libfm-qt \
			x11/dbusmenu-qt,qt5

BUILD_DEPENDS +=	x11/lxqt/build-tools

RUN_DEPENDS +=		x11/lxqt/liblxqt

CONFIGURE_ENV +=	Qt5Widgets_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5LinguistTools_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5DBus_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5Svg_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5X11Extras_DIR=${LOCALBASE}/lib/qt5/cmake

.include <bsd.port.mk>
