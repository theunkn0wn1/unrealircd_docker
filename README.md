# unrealircd_docker

This project defines a UnrealIRCd server coupled with Anope IRC services.

# WARNING
This image is _**NOT**_ intended for production use! Its primary function is to provide a 
bare-minimum IRC server w services to facilitate in testing IRC clients.
It is NOT configured for use in production applications.

---------------------
## Docker-compose
This project is set up with two containers, `irc` and `services`

`irc` contains the UnrealIRCd itself, which exposes insecure port `6667` and "secure" port `6697` to the host.
These ports are where you should connect the irc client under test via.

`services` contains the Anope IRC services server. It is configured to connect to `irc:6900` on startup


