# This image is based on "debian:stretch"
FROM postgres:10

RUN set -x \
    && apt-get update && apt-get install -y --no-install-recommends \
        python3 \
        python3-pip \
        python3-setuptools \
        lzop \
        pv \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install -U pip \
    && pip3 install --no-cache-dir wal-e[azure]