FROM docker.io/centos
MAINTAINER 2367192101@qq.com

ENV TZ "Asia/Shanghai"

ADD simkai.ttf /usr/share/fonts/
ADD simsun.ttf /usr/share/fonts/

# Use the aliyun mirror.
RUN curl http://mirrors.aliyun.com/repo/Centos-7.repo >> /etc/yum.repos.d/CentOS-Base.repo && \
    ln -snf /usr/share/zoneinfo/${TZ} /etc/localtime && echo ${TZ} > /etc/timezone && \
     yum install -y fontconfig xorg-x11-font-utils yum install kde-l10n-Chinese  && \
     yum reinstall -y glibc-common && \
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

