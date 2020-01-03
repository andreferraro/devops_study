FROM debian

RUN apt-get update
RUN apt-get install -y apt-utils
RUN apt-get install -y openssl

ENV OPENSSL_SUBJ="/C=BR/ST=Sao Paulo/L=Campinas"
ENV OPENSSL_CA="${OPENSSL_SUBJ}/CN=main-CA"
ENV OPENSSL_SERVER="${OPENSSL_SUBJ}/CN=main-server"
ENV OPENSSL_CLIENT="${OPENSSL_SUBJ}/CN=main-client"

COPY gencerts.sh /
RUN chmod +x /gencerts.sh

VOLUME /certs

WORKDIR /certs

CMD /gencerts.sh