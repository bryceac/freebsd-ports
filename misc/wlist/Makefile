PORTNAME=	wlist
DISTVERSIONPREFIX=	v
DISTVERSION=	0.2.0
CATEGORIES=	misc

MAINTAINER=	tonyhawk2100@gmail.com
COMMENT=	Tool to create a wishlist
WWW=	https://github.com/bryceac/wlist

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=	cargo llvm:lib

USE_GITHUB=	yes
GH_ACCOUNT=	bryceac

MAKE_ENV=	LIBCLANG_PATH=${LLVM_PREFIX}/lib

PLIST_FILES=	bin/${PORTNAME}

do-install:
	${INSTALL_PROGRAM} ${WRKDIR}/target/release/wlist \
		${STAGEDIR}${PREFIX}/bin

.include <bsd.port.mk>
