# $OpenBSD$

V =		0.0.2
COMMENT =	DeforaOS Desktop PDF viewer
DISTNAME =	deforaos-pdfviewer-${V}

GH_PROJECT =	PDFViewer
GH_TAGNAME =	PDFViewer_${V:S/./-/g}

# BSD
PERMIT_PACKAGE_CDROM =	Yes

WANTLIB += Desktop System X11 Xcomposite Xcursor Xdamage Xext
WANTLIB += Xfixes Xi Xinerama Xrandr Xrender atk-1.0 c cairo fontconfig
WANTLIB += freetype gdk-x11-2.0 gdk_pixbuf-2.0 gio-2.0 glib-2.0
WANTLIB += gobject-2.0 gtk-x11-2.0 intl m pango-1.0 pangocairo-1.0
WANTLIB += pangoft2-1.0 poppler-glib z

BUILD_DEPENDS =	devel/gettext-tools \
		textproc/libxslt

LIB_DEPENDS =	print/poppler \
		x11/deforaos/libdesktop

RUN_DEPENDS =	devel/desktop-file-utils

# The usual
pre-configure:
	cd ${WRKSRC} && grep -Rl '\-O2' * | xargs sed -i 's,-O2,${CFLAGS},g'

do-configure:
	cd ${WRKSRC} && ${LOCALBASE}/bin/configure
	@cp ${FILESDIR}/doc-Makefile ${WRKSRC}/doc/Makefile

.include <bsd.port.mk>
