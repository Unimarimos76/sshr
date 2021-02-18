FROM kinogmt/centos-ssh

RUN useradd fuga && \
    echo "fuga:testpass" | chpasswd && \
    mkdir -p /home/fuga/.ssh

ADD misc/testdata/sshr_keys/id_rsa.pub /home/fuga/.ssh

RUN touch /home/fuga/.ssh/authorized_keys && \
    chown fuga:fuga /home/fuga/.ssh/authorized_keys && \
    chmod 600 /home/fuga/.ssh/authorized_keys && \
    cat /home/fuga/.ssh/id_rsa.pub > /home/fuga/.ssh/authorized_keys
