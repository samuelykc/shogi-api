FROM amazonlinux:2.0.20230912.0

RUN yum install -y gcc gcc-c++ make build-essential git

WORKDIR /work
COPY Makefile Makefile

CMD git clone https://github.com/yaneurao/YaneuraOu.git -b V7.61 && \
    cp Makefile YaneuraOu/source/ && \
    cd YaneuraOu/source && make normal && \
    mv YaneuraOu-by-gcc /out/YO761-sse42
