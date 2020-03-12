# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lubenard <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/03/12 11:59:00 by lubenard          #+#    #+#              #
#    Updated: 2020/03/12 12:11:43 by lubenard         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu
RUN apt-get update && apt-get upgrade -y && apt install -y wget openjdk-11-jdk
RUN wget https://launcher.mojang.com/v1/objects/bb2b6b1aefcd70dfd1892149ac3a215f6c636b07/server.jar
RUN java -Xmx1024M -Xms1024M -jar server.jar nogui
RUN echo "eula=true" > eula.txt
ENTRYPOINT java -Xmx1024M -Xms1024M -jar server.jar nogui

## How to build it
# docker build -t minecraft .
## How to launch it
# docker run -it -p 25565:25565 minecraft_server
