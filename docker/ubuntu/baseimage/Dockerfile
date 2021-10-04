FROM phusion/baseimage:bionic-1.0.0

COPY ./bootstrap.sh /bootstrap.sh
RUN /bootstrap.sh && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

COPY ./install_lint.sh /root/install_lint.sh
COPY ./install_luarocks.sh /root/install_luarocks.sh
COPY .bashrc /root/.bashrc

WORKDIR /root
RUN ./install_lint.sh
RUN ./install_luarocks.sh
