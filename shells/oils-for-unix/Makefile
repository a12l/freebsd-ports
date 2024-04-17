PORTNAME=	oils-for-unix
DISTVERSION=	0.21.0
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
INTERACTIVE_USES=		readline
INTERACTIVE_CONFIGURE_WITH=	readline
INTERACTIVE_CONFIGURE_ARGS=	--readline=${LOCALBASE}
  
BUILD_DEPENDS=	bash:shells/bash

PLIST_FILES=	bin/osh \
		bin/ysh

.include <bsd.port.mk>
