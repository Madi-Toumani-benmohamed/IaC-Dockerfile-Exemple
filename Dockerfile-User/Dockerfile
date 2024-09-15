FROM debian:buster-slim
LABEL maintainer="ben@ben.fr"
RUN groupadd -g 10001 noroot && \
    useradd -g noroot -u 1001 ben -m -s /home/ben/

RUN apt-get update -y \
    && apt-get install -y iputils-ping dnsutils net-tools \
    && apt-get remove --purge --auto-remove -y \
    && rm -rf /var/lib/apt/lists/*
USER ben
CMD ["ping" , "1.1.1.1" ]
