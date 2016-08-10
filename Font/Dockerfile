FROM docker.io/centos
MAINTAINER 2367192101@qq.com

ADD simkai.ttf /usr/share/fonts/
ADD simsun.ttf /usr/share/fonts/
RUN  yum install -y fontconfig xorg-x11-font-utils yum install kde-l10n-Chinese  && \
     yum reinstall -y glibc-common && \
     /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
     mkdir /usr/share/fonts/simkai && \
     mkdir /usr/share/fonts/simsun && \
     mv /usr/share/fonts/simkai.ttf /usr/share/fonts/simkai/ && \
     mv /usr/share/fonts/simsun.ttf /usr/share/fonts/simsun/ && \
     cd /usr/share/fonts/simkai/ && \ 
     mkfontscale && \
     mkfontdir && \
     cd /usr/share/fonts/simsun && \
     mkfontscale && \
     mkfontdir && \
     yum clean all

