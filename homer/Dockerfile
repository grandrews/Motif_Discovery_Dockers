FROM ubuntu:16.04
RUN apt-get update && apt-get install -y \
    gcc \
    g++ \
    make \
    perl \
    wget \
    zip \
    unzip

RUN mkdir /opt/homer
ADD http://homer.ucsd.edu/homer/configureHomer.pl /opt/homer
WORKDIR /opt/homer
RUN perl configureHomer.pl -install
ENV PATH="/opt/homer/bin:${PATH}"

ENTRYPOINT ["findMotifs.pl"]