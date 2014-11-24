FROM fedora:latest
RUN yum install -y nc
CMD ncat -l 2000 -k -c 'xargs -n1 echo'
