FROM mysql:5.6
RUN apt-get update && apt-get install wget -y
RUN cd /docker-entrypoint-initdb.d && \
    wget http://homologacao.minerais-mg.com.br/00-rmmg-site-schema.sql && \
    wget http://homologacao.minerais-mg.com.br/01-rmmg-site-dados.sql
RUN cd /docker-entrypoint-initdb.d && \
    sed -i 's/\/rmmg-site/\/html/g' 01-rmmg-site-dados.sql && \
    sed -i "s/homologacao.minerais-mg.com.br/200.198.55.108/g" 01-rmmg-site-dados.sql && \
    sed -i "s/minerais-mg.com.br/200.198.55.108/g" 01-rmmg-site-dados.sql
