# $OpenBSD$

COMMENT =	information about LXQt and the system its running on

VERSION =	0.13.0

NAME=		lxqt-about
DISTNAME =	${NAME}-${VERSION}

WANTLIB += ${COMPILER_LIBCXX} KF5WindowSystem Qt5Core Qt5DBus
WANTLIB += Qt5Gui Qt5Svg Qt5Widgets Qt5X11Extras Qt5Xdg Qt5XdgIconLoader
WANTLIB += Qt5Xml c lxqt m

LIB_DEPENDS +=		x11/lxqt/liblxqt

RUN_DEPENDS +=		devel/desktop-file-utils \
			x11/lxqt/l10n,-about

CONFIGURE_ARGS +=	-DPULL_TRANSLATIONS:BOOL=OFF
CONFIGURE_ENV +=	Qt5Widgets_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5DBus_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5X11Extras_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5LinguistTools_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5Xml_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5Svg_DIR=${LOCALBASE}/lib/qt5/cmake

.include <bsd.port.mk>
