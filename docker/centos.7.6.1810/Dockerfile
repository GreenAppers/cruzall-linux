FROM centos:7.6.1810
LABEL maintainer="support@greenappers.com"

RUN yum install -y epel-release && \
    yum install -y centos-release-scl && \
    rpm -U https://centos7.iuscommunity.org/ius-release.rpm && \
    yum install -y which git2u unzip llvm-toolset-7-clang openssl-devel \
    bzip2-devel libpng-devel libjpeg-devel freetype-devel fontconfig-devel \
    gtk3-devel mesa-libGL-devel mesa-libGLU-d libXrandr-devel libXi-devel \
    libXv-devel libXt-devel libXcursor-devel redhat-lsb rpm-build \
    mesa-dri-drivers rsync

RUN echo "source scl_source enable devtoolset-7 llvm-toolset-7" >> /root/.bashrc
RUN echo "export PATH=\$PATH:/root/flutter/bin" >> /root/.bashrc

ENV PACKAGE_INSTALL yum -y install
ENV PACKAGE_SUFFIX rpm
