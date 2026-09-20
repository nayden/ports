GH_ACCOUNT =	fabianishere
GH_PROJECT =	brainfuck
GH_TAGNAME =	2.7.3

COMMENT =	Brainfuck interpreter written in C
CATEGORIES =	lang

MAINTAINER =	Nayden Markatchev <nayden@openbsd.org>

# Apache 2.0
PERMIT_PACKAGE =	Yes

WANTLIB += c curses edit

MODULES =	devel/cmake

NO_TEST =	Yes

MODCMAKE_POLICY_VERSION_OVERRIDE = Yes

EXAMPLESDIR=${PREFIX}/share/examples/brainfuck/examples

post-install:
	${INSTALL_DATA_DIR} ${EXAMPLESDIR} ${EXAMPLESDIR}/asciiart \
	${EXAMPLESDIR}/bench \
	${EXAMPLESDIR}/compiler \
	${EXAMPLESDIR}/interpreter \
	${EXAMPLESDIR}/mandelbrot \
	${EXAMPLESDIR}/math \
	${EXAMPLESDIR}/quine \
	${EXAMPLESDIR}/sort

	cd ${WRKSRC}/examples/ && cp -p *.bf ${EXAMPLESDIR}
#	cd ${WRKSRC}/examples/ && cp -p asciiart/*.bf ${EXAMPLESDIR}/asciiart
#	cd ${WRKSRC}/examples/ && cp -p bench/*.bf ${EXAMPLESDIR}/bench
#	cd ${WRKSRC}/examples/ && cp -p compiler/*.bf ${EXAMPLESDIR}/compiler
#	cd ${WRKSRC}/examples/ && cp -p *.bf ${EXAMPLESDIR}
#	cd ${WRKSRC}/examples/ && cp -p *.bf ${EXAMPLESDIR}
#	cd ${WRKSRC}/examples/ && cp -p *.bf ${EXAMPLESDIR}
#	cd ${WRKSRC}/examples/ && cp -p *.bf ${EXAMPLESDIR}

.include <bsd.port.mk>
