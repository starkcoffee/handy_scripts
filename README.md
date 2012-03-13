# Handy Scripts

handy handy!

## tcpspy

A simple proxy using netcat I use to see actual http traffic without having to start wireshark or charlesproxy .
Since it is simply showing the tcp payload, it won't help you if you are using ssl or gzip - charlesproxy is good here.

It logs traffic to file called http.log. This is a bit of an assumption :)


    tcpspy your_server_host your_server_port [tcpspy_port - 6060 by default]"
    GET http://localhost:6060/yourapp

I notice that browing traffic in firefox leaves the tcpspy listening, whereas using curl kills tcpspy - could be a keep-alive thing?

Also, if it's not working and just hanging there.. check there is nothing else listening on that port - later version will do a check.

Tested on Mac OS 10.6
