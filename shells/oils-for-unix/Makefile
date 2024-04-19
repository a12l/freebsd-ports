PORTNAME=	oils-for-unix
DISTVERSION=	0.23.0
CATEGORIES=	shells
MASTER_SITES=	https://www.oilshell.org/download/

MAINTAINER=	freebsd@a12l.se
COMMENT=	Oils is a Unix shell with JSON-compatible structured data. It's our upgrade path from bash to a better language and runtime.
WWW=		https://www.oilshell.org

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

GNU_CONFIGURE=yes

USES=		gmake localbase

OPTIONS_DEFINE=			INTERACTIVE
OPTIONS_DEFAULT=		INTERACTIVE

INTERACTIVE_DESC=		Include Oils CLI
  
BUILD_DEPENDS=	bash:shells/bash

PLIST_FILES=	bin/osh \
		bin/ysh

do-build:
	@cd ${WRKSRC}/ && ${SETENV} -i ${MAKE_ENV} ${SH} bin/package flat make
	cd ${WRKSRC}/_build/oils.sh

do-install:
	./install

.include <bsd.port.mk>
