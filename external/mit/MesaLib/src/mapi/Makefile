#	$NetBSD$

# generate format_srgb.c

.include "../Makefile.inc"

SCRIPT=	${X11SRCDIR.MesaLib}/src/mapi/mapi_abi.py
XML=	${X11SRCDIR.MesaLib}/src/mapi/glapi/gen/gl_and_es_API.xml

shared-glapi_glapi_mapi_tmp.h: ${SCRIPT} ${XML}
	${PYTHON} ${SCRIPT} --mode lib --printer shared-glapi ${XML} > $@.tmp && mv $@.tmp $@

# XXX this seems duplicated
