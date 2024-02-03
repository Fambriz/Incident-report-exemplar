# Incident-report-exemplar
Analyzing Network Attacks

Type of attack causing the website issue.

One possible reason for the website showing a connection timeout error could be a DoS attack. The logs reveal that the web server stops working when it gets bombarded with SYN packet requests. This kind of DoS attack is known as SYN flooding.

How the attack messes up the website.

When people try to connect to the web server, they do a three-step handshake using the TCP protocol:

A request (SYN packet) is sent to connect.
The server replies (SYN-ACK packet) to accept the connection and reserves resources.
The requester acknowledges (ACK packet) the permission to connect.
In a SYN flood attack, a bad actor sends tons of SYN packets at once, overwhelming the server's resources reserved for connections. As a result, there are no resources left for real connection requests.

The logs show the server getting overwhelmed, unable to handle the SYN requests from visitors. New people trying to connect get a timeout message because the server can't open a new connection for them
