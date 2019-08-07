#! /bin/env python

Import('defconfig')


lib_name = 'websocket'

source_files = [
    Glob('src/*.c')
]

include_paths = [
    'include',
    '../mbedtls/configs'
]

# Build library
installs = [
	('include', Glob('include/*.h'))
]

L_CFLAGS = "-DCONFIG_USING_TLS"
L_CFLAGS += " -g -O0"

# Build library
defconfig.library(lib_name, source_files, CCFLAGS=L_CFLAGS, CPPPATH=include_paths, INSTALL=installs)
