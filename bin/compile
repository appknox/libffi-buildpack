#! /bin/bash
#
# compile.sh
# Copyright (C) 2016 subho <subho@appknox>
#
# Distributed under terms of the MIT license.
#


echo "Building libffi..."

SOURCE_TARBALL='https://cl.ly/2s1t1u3v0N0I/download/libffi-3.1.tar'
OUT_PREFIX="/app/.appknox/vendor/"
PKG_CONFIG_PATH="/app/.appknox/vendor/lib/pkgconfig:$PKG_CONFIG_PATH"

mkdir -p /app/.appknox/vendor

curl $SOURCE_TARBALL -s | tar zxv -C .heroku/vendor &> /dev/null

cd libffi-3.1
./autogen.sh
./configure --prefix=$OUT_PREFIX --disable-static && make && make install

cd ..
