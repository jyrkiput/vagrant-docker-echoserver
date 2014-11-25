Demonstrating docker provisioner. Set up two containers, a server and a proxy. The server is simple echo and proxy, well, is a proxy. Server listens to port 2000, and proxy listens to port 3000. You can telnet to either one of those.

To test this, run:

    vagrant up --provider docker
    telnet localhost 3000
