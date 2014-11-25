FROM fedora:latest
RUN yum install -y socat
CMD ["/usr/bin/socat", "TCP-LISTEN:3000,fork", "TCP:server:2000"]
