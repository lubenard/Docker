# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lubenard <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/02/12 15:29:34 by lubenard          #+#    #+#              #
#    Updated: 2020/03/11 17:57:47 by lubenard         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu
ARG DEBIAN_FRONTEND=noninteractive
EXPOSE 443 80 22
RUN apt-get update && apt-get upgrade -y && apt-get install -y apt-utils git ruby curl wget openssh-server ca-certificates postfix tzdata
RUN curl -sL https://deb.nodesource.com/setup_13.x | bash -
RUN apt-get install -y nodejs
RUN curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | bash
RUN apt-get install -y gitlab-ce
ENV EXTERNAL_URL="https://gitlab.localhost"
RUN (/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure
ENTRYPOINT (/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl start && bash

## How to build it
# docker build -t gitlab .
##NOTE: please build it on bigger VM ! (why ? ELse Grafana fail...)
# here is how to create one
# docker-machine create --driver virtualbox --virtualbox-cpu-count "2" --virtualbox-memory "4096" CharBig
# eval $(docker-machine env CharBig)
## How to launch it
# docker run -it -p 8443:443 -p 8080:80 -p 8022:22 gitlab
