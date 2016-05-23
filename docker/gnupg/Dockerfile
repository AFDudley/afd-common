FROM alpine:3.3
MAINTAINER Eris Industries <support@erisindustries.com>

RUN apk update; apk add make gcc musl-dev openssl

RUN mkdir code
WORKDIR code

RUN wget https://www.gnupg.org/ftp/gcrypt/libgpg-error/libgpg-error-1.22.tar.bz2 && \
    tar -jxf libgpg-error-1.22.tar.bz2 && \
    cd libgpg-error-1.22 && ./configure && make install

RUN wget https://www.gnupg.org/ftp/gcrypt/libgcrypt/libgcrypt-1.7.0.tar.bz2 && \
    tar -jxf libgcrypt-1.7.0.tar.bz2 && \
    cd libgcrypt-1.7.0 && ./configure && make install

RUN wget https://www.gnupg.org/ftp/gcrypt/libksba/libksba-1.3.4.tar.bz2 && \
    tar -jxf libksba-1.3.4.tar.bz2 && \
    cd libksba-1.3.4 && ./configure && make install

RUN wget https://www.gnupg.org/ftp/gcrypt/libassuan/libassuan-2.4.2.tar.bz2 && \
    tar -jxf libassuan-2.4.2.tar.bz2 && \
    cd libassuan-2.4.2 && ./configure && make install

RUN wget https://www.gnupg.org/ftp/gcrypt/npth/npth-1.2.tar.bz2 && \
    tar -jxf npth-1.2.tar.bz2 && \
    cd npth-1.2 && ./configure && make install

# RUN wget https://www.gnupg.org/ftp/gcrypt/pinentry/pinentry-0.9.7.tar.bz2 && \
#     tar -jxf pinentry-0.9.7.tar.bz2 && \
#     cd pinentry-0.9.7 && ./configure && make install

RUN wget https://www.gnupg.org/ftp/gcrypt/gnupg/gnupg-2.1.12.tar.bz2 && \
    tar -jxf gnupg-2.1.12.tar.bz2 && \
    cd gnupg-2.1.12 && ./configure && make install
    


# we have to check sigs after we build :D
# RUN wget https://www.gnupg.org/ftp/gcrypt/gnupg/gnupg-2.1.12.tar.bz2.sig && \
#     wget https://www.gnupg.org/ftp/gcrypt/libgpg-error/libgpg-error-1.22.tar.bz2.sig && \
#     wget https://www.gnupg.org/ftp/gcrypt/libgcrypt/libgcrypt-1.7.0.tar.bz2.sig && \
#     wget https://www.gnupg.org/ftp/gcrypt/libksba/libksba-1.3.4.tar.bz2.sig && \
#     wget https://www.gnupg.org/ftp/gcrypt/libassuan/libassuan-2.4.2.tar.bz2.sig && \
#     wget https://www.gnupg.org/ftp/gcrypt/npth/npth-1.2.tar.bz2.sig && \
#     wget https://www.gnupg.org/ftp/gcrypt/pinentry/pinentry-0.9.7.tar.bz2.sig

