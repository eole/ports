# $FreeBSD$

PORTNAME=	fastdfs
DISTVERSION=	6.0.6
CATEGORIES=	ftp
PKGNAMEPREFIX=	${PHP_PKGNAMEPREFIX}

MAINTAINER=	daniel@blodan.se
COMMENT=	PHP module for accessing a FastDFS cluster

LICENSE=	GPLv3+

LIB_DEPENDS=	libfastcommon.so:devel/libfastcommon \
		libfdfsclient.so:ftp/fastdfs

USES=		php:ext
IGNORE_WITH_PHP=	80

USE_GITHUB=	yes
GH_ACCOUNT=	happyfish100
GH_PROJECT=	fastdfs
GH_TAGNAME=	V6.06

WRKSRC_SUBDIR=	php_client
CONFIGURE_ENV=	ROOT=${LOCALBASE}

PHP_MODNAME=	fastdfs_client

.include <bsd.port.mk>
