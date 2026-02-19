# IPv6-guide-for-Plex
A Guide to stream Plex over IPv6

TLDR: got put behind CGNAT, sister couldn't access my server anymore. Used random guides and AI to piece together a fix.

Get servers IPv6 by typing ipconfig /all into terminal/cmd, eg (2af1:8045:f94d:adcf:5def:4b08:1b8f:16ae)

Go to your Routers IPv6 firewall and allow port 32400 on your IPv6 address.

Go to https://www.duckdns.org/, create an account, create your custom url and paste in the servers IPv6 address and press 'update ipv6'.

Go to Plex server, Settings > Network > Custom server access URLs

and paste in http://YOURCUSTOMURL.duckdns.org:32400, https://YOURCUSTOMURL.duckdns.org:32400

If you don't use a custom URL and just input the IPv6 address directly, Plex will briefly connect but then throw you away back to their homepage.

If you can be bothered, you can run a .bat script with task scheduler to auto update your IPv6 address in case it changes and update DuckDNS.

https://github.com/mbtechtt/DuckDNS-IPV4-IPV6

Hope that helps some people because I couldn't find all the info from one source.
