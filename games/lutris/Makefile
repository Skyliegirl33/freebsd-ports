PORTNAME=		lutris
DISTVERSION=	0.5.10.2	
CATEGORIES=		games python
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=		skyliegirl33@protonmail.com
COMMENT=		Video game preservation platform

LICENSE=		GPLv3+
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	gettext:devel/gettext \
				appstream-util:devel/appstream-glib \
				meson:devel/meson \
				ninja:devel/ninja		
LIB_DEPENDS=	libvulkan.so:graphics/vulkan-loader \
				libwebkit2gtk-4.0.so:www/webkit2-gtk3 \
				libgnome-desktop-4.so:x11/gnome-desktop \
				libglib-2.0.so:devel/glib20
RUN_DEPENDS=	cabextract:archivers/cabextract \
				curl:ftp/curl \
				glxinfo:graphics/mesa-demos \
				killall:sysutils/psmisc \
				xrandr:x11/xrandr \
				unzip:archivers/unzip \
				${PYTHON_PKGNAMEPREFIX}dbus>0:devel/py-dbus@${PY_FLAVOR} \
				${PYTHON_PKGNAMEPREFIX}evdev>0:devel/py-evdev@${PY_FLAVOR} \
				${PYTHON_PKGNAMEPREFIX}gobject3>0:devel/py-gobject3@${PY_FLAVOR} \
				${PYTHON_PKGNAMEPREFIX}yaml>0:devel/py-yaml@${PY_FLAVOR} \
				${PYTHON_PKGNAMEPREFIX}lxml>0:devel/py-lxml@${PY_FLAVOR} \
				${PYTHON_PKGNAMEPREFIX}pillow>0:graphics/py-pillow@${PY_FLAVOR} \
				${PYTHON_PKGNAMEPREFIX}distro>0:sysutils/py-distro@${PY_FLAVOR} \
				${PYTHON_PKGNAMEPREFIX}setproctitle>0:devel/py-setproctitle@${PY_FLAVOR}
				
USES=			shebangfix gnome meson python:3.7+ desktop-file-utils
USE_MESON=		ninja python:3.7+,build,run
USE_GNOME=		pygobject3
USE_PYTHON=		noflavors cython
USE_GITHUB=		yes
GH_ACCOUNT=		Skyliegirl33
GH_PROJECT=		lutris
GH_TAGNAME=		v0.5.10.2

SHEBANG_FILES=	bin/lutris share/lutris/bin/lutris-wrapper

.include <bsd.port.mk>
