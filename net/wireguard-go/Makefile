# $FreeBSD$

PORTNAME=	wireguard-go
PORTVERSION=	0.0.20210212
PORTEPOCH=	1
CATEGORIES=	net net-vpn
MASTER_SITES=	https://git.zx2c4.com/wireguard-go/snapshot/
DISTFILES=	${PORTNAME}-${PORTVERSION}${EXTRACT_SUFX}

MAINTAINER=	decke@FreeBSD.org
COMMENT=	WireGuard implementation in Go

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		gmake go:modules,no_targets tar:xz

USE_GITHUB=	nodefault
GH_TUPLE=	golang:crypto:eec23a3978ad:golang_crypto/vendor/golang.org/x/crypto \
		golang:net:6772e930b67b:golang_net/vendor/golang.org/x/net \
		golang:sys:16f7687f5001:golang_sys/vendor/golang.org/x/sys

MAKE_ENV+=	${GO_ENV} GOFLAGS="${GO_BUILDFLAGS}"

PLIST_FILES=	bin/${PORTNAME}

.include <bsd.port.mk>
