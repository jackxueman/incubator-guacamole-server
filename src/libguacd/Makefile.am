#
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.
#

AUTOMAKE_OPTIONS = foreign 

noinst_LTLIBRARIES = libguacd.la

noinst_HEADERS =    \
    libguacd/log.h  \
    libguacd/user.h

libguacd_la_SOURCES = \
    log.c             \
    user.c

libguacd_la_CFLAGS =        \
    -Werror -Wall -pedantic \
    @COMMON_INCLUDE@        \
    @LIBGUAC_INCLUDE@

libguacd_la_LIBADD = \
    @COMMON_LTLIB@   \
    @LIBGUAC_LTLIB@

libguacd_la_LDFLAGS = \
    @PTHREAD_LIBS@    \
    @SSL_LIBS@

# SSL support
if ENABLE_SSL
noinst_HEADERS      += libguacd/socket-ssl.h
libguacd_la_SOURCES += socket-ssl.c
endif

