# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lubenard <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/03/11 18:24:02 by lubenard          #+#    #+#              #
#    Updated: 2020/03/12 13:45:06 by lubenard         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ruby
EXPOSE 3000
RUN apt update && apt upgrade -y && apt install -y tzdata yarn nodejs postgresql-client
RUN gem install rails
ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed

## How to build it
# docker build -t ruby .
## how to launch it
# docker run -p 3000:3000 ruby
