PORTNAME=	kurama
DISTVERSIONPREFIX=	v
DISTVERSION=	0.4.1
CATEGORIES=	www

MAINTAINER=	dev@kurama.cc
COMMENT=	Static generator for regular websites
WWW=	https://kurama.cc

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=	cargo llvm:lib

USE_GITHUB=	yes
GH_ACCOUNT=	bryceac

MAKE_ENV=	LIBCLANG_PATH=${LLVM_PREFIX}/lib

PLIST_FILES=	bin/${PORTNAME}

do-install:
	${INSTALL_PROGRAM} ${WRKDIR}/target/release/kurama \
		${STAGEDIR}${PREFIX}/bin

.include <bsd.port.mk>
