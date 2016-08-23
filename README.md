# pacemaker

Custom RA for delaying systemd process return . 
This is a systemd process Resource Agent designed to delay the return on processes
that start other processes so that everything is actually ready when the 
RA is returning "Started".
This RA was created with Tomcat running Solr in mind. 
The delay can be either timed (startdelay) or set to curl an url-header and 
return when it succeeds (url).
It is based on the ocf: heartbeat:Delay RA and the ocf: heartbeat:Dummy RA.

I take no responsibilty whatsoever for what happens if you use it.
