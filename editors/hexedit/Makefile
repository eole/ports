# Created by: Andrey Zakhvatov
# $FreeBSD$

PORTNAME=	hexedit
PORTVERSION=	1.5
CATEGORIES=	editors

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	View and edit files in hexadecimal or ASCII

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		autoreconf ncurses

USE_HARDENING=	safestack

GNU_CONFIGURE=	yes

PLIST_FILES=	bin/hexedit share/man/man1/hexedit.1.gz

GH_ACCOUNT=	pixel
USE_GITHUB=	yes

post-build:
	m4 -DVERSION=${PORTVERSION} ${WRKSRC}/hexedit.1.in > ${WRKSRC}/hexedit.1

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin/
	${INSTALL_MAN} ${WRKSRC}/${PORTNAME}.1 ${STAGEDIR}${PREFIX}/share/man/man1/

.include <bsd.port.mk>
