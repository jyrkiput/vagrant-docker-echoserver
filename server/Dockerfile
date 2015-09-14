FROM fedora:23
RUN dnf install -y nc findutils
CMD ncat -l 2000 -k -c 'xargs -n1 echo'
