FROM alpine:3.4
MAINTAINER Eris Industries <support@erisindustries.com>

RUN apk update; apk add git bash musl-dev jq build-base sc gmp-dev g++ python-dev cmake curl yaml-dev
#    lllc \
#    solc && \

#boost-dev is the wrong package... optimize later.

RUN apk update; apk add boost-dev jsoncpp-dev

RUN mkdir /code
WORKDIR /code

#RUN git clone https://github.com/weidai11/cryptopp && cd cryptopp/ &&\
#    git checkout 298988a5b9687f64de733ce01319e90e94b0b688 &&\
#    make; make install

RUN git clone https://github.com/AFDudley/solidity.git --branch solidity_standalone --single-branch; ls

#RUN cd solidity; mkdir -p build; cd build; cmake .. -DEVMJIT=0 -DTESTS=0 -DGUI=0 -DSTATIC_LINKING=1


# ugh just use: https://github.com/AFDudley/solidity-static/blob/master/Dockerfile