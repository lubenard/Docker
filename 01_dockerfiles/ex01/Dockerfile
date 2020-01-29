# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lubenard <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/01/29 13:23:50 by lubenard          #+#    #+#              #
#    Updated: 2020/01/29 14:18:09 by lubenard         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian
RUN apt update && apt upgrade -y && apt install -y wget lbzip2
RUN wget -O teamspeak-server https://files.teamspeak-services.com/releases/server/3.11.0/teamspeak3-server_linux_amd64-3.11.0.tar.bz2
RUN tar -jxf teamspeak-server
ENV TS3SERVER_LICENSE=accept
RUN ./teamspeak3*/server_minimal_runscript.sh
