# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lubenard <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/01/29 13:20:07 by lubenard          #+#    #+#              #
#    Updated: 2020/03/10 17:36:55 by lubenard         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM alpine
RUN apk update && apk upgrade && apk add vim
ENTRYPOINT vim

## To build it
# docker build -t vim .
## To launch it
# docker run -it vim
