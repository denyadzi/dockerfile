FROM ubuntu:14.04

RUN apt-get update && apt-get -y install software-properties-common \
    && DEBIAN_FRONTEND=noninteractive add-apt-repository -y ppa:ondrej/php \
    && apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E5267A6C

RUN apt-get update && apt-get install -y php7.0-cli   \
                       php7.0-common  \
                       php7.0-curl  \
                       php7.0-mysql \
                       php7.0-gd    \ 
                       php7.0-xmlrpc

CMD ["php", "/app/scripts/warehouse/task_manager.php", "--url", "mirtrik.local"]

