# $OpenBSD$

COMMENT =	lxqt notification daemon

VERSION =	0.13.0

NAME=		lxqt-notificationd
DISTNAME =	${NAME}-${VERSION}

WANTLIB += ${COMPILER_LIBCXX} KF5WindowSystem Qt5Core Qt5DBus
WANTLIB += Qt5Gui Qt5Svg Qt5Widgets Qt5X11Extras Qt5Xdg Qt5XdgIconLoader
WANTLIB += Qt5Xml c lxqt m

LIB_DEPENDS +=		x11/lxqt/liblxqt \
			devel/kf5/kwindowsystem

BUILD_DEPENDS +=	x11/lxqt/build-tools

RUN_DEPENDS +=		devel/desktop-file-utils \
			x11/lxqt/l10n,-notificationd

CONFIGURE_ARGS +=	-DPULL_TRANSLATIONS:BOOL=OFF
CONFIGURE_ENV +=	Qt5Widgets_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5LinguistTools_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5DBus_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5X11Extras_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5Xml_DIR=${LOCALBASE}/lib/qt5/cmake
CONFIGURE_ENV +=	Qt5Svg_DIR=${LOCALBASE}/lib/qt5/cmake

post-install:
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/${NAME}
	mv ${WRKINST}${SYSCONFDIR}/xdg ${PREFIX}/share/examples/${NAME}/

.include <bsd.port.mk>
