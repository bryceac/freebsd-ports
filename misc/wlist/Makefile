PORTNAME=	wlist
DISTVERSIONPREFIX=	v
DISTVERSION=	0.3.2
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
MANDIR=	${LOCALBASE}/share/man/man1

PLIST_FILES=	bin/${PORTNAME} \
	${MANDIR}/wlist.1.gz \
	${MANDIR}/wlist-add.1.gz \
	${MANDIR}/wlist-delete.1.gz \
	${MANDIR}/wlist-export.1.gz \
	${MANDIR}/wlist-import.1.gz \
	${MANDIR}/wlist-show.1.gz \
	${MANDIR}/wlist-update.1.gz

do-install:
	${MKDIR} ${STAGEDIR}${MANDIR}
	${INSTALL_PROGRAM} ${WRKDIR}/target/release/wlist \
		${STAGEDIR}${PREFIX}/bin
	${INSTALL_DATA} ${WRKSRC}/man/wlist.1 \
		${STAGEDIR}${MANDIR}
	${INSTALL_DATA} ${WRKSRC}/man/wlist-add.1 \
		${STAGEDIR}${MANDIR}
	${INSTALL_DATA} ${WRKSRC}/man/wlist-delete.1 \
		${STAGEDIR}${MANDIR}
	${INSTALL_DATA} ${WRKSRC}/man/wlist-export.1 \
		${STAGEDIR}${MANDIR}
	${INSTALL_DATA} ${WRKSRC}/man/wlist-import.1 \
		${STAGEDIR}${MANDIR}
	${INSTALL_DATA} ${WRKSRC}/man/wlist-show.1 \
		${STAGEDIR}${MANDIR}
	${INSTALL_DATA} ${WRKSRC}/man/wlist-update.1 \
		${STAGEDIR}${MANDIR}

.include <bsd.port.mk>
