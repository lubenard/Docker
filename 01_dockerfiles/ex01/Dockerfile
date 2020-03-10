# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lubenard <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/01/29 13:23:50 by lubenard          #+#    #+#              #
#    Updated: 2020/03/10 18:25:24 by lubenard         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian
RUN apt-get update && apt-get upgrade -y && apt-get install -y wget bzip2
RUN wget -O teamspeak-server https://files.teamspeak-services.com/releases/server/3.11.0/teamspeak3-server_linux_amd64-3.11.0.tar.bz2
RUN tar -jxf teamspeak-server
ENV TS3SERVER_LICENSE=accept
ENTRYPOINT ./teamspeak3*/ts3server_minimal_runscript.sh

## To build it
# docker build -t teamspeak .
## How to build it
# docker run -it -p 9987:9987/udp -p 10011:10011 -p 30033:30033 teamspeak
