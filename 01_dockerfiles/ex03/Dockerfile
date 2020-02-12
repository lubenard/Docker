# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lubenard <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/02/12 15:29:34 by lubenard          #+#    #+#              #
#    Updated: 2020/02/12 16:04:31 by lubenard         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu
ENV GOROOT=/usr/local/go
ENV GOPATH=/git
RUN apt update && apt upgrade -y && apt install -y git ruby curl wget openssh-server ca-certificates postfix tzdata
RUN wget https://dl.google.com/go/go1.13.3.linux-amd64.tar.gz
RUN curl -sL https://deb.nodesource.com/setup_13.x | bash -
RUN apt install -y nodejs
RUN curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ee/script.deb.sh | bash
RUN /opt/gitlab/embedded/bin/runsvdir-start &
RUN EXTERNAL_URL="https://gitlab.localost" apt-get install gitlab-ee
