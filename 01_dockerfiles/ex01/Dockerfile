FROM debian

RUN apt-get update -y && apt-get upgrade -y 
RUN apt-get install curl -y 
RUN apt-get install bzip2 -y 
RUN curl -O http://dl.4players.de/ts/releases/3.1.0/teamspeak3-server_linux_amd64-3.1.0.tar.bz2
RUN bzip2 -d teamspeak3-server_linux_amd64-3.1.0.tar.bz2
RUN tar -xf teamspeak3-server_linux_amd64-3.1.0.tar

EXPOSE 9987/udp
EXPOSE 10011
EXPOSE 30033

ENV TS3SERVER_LICENSE accept

ENTRYPOINT sh ./teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh