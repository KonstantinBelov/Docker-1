# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: kbelov <marvin@42.fr>                      +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/07/27 23:06:26 by kbelov            #+#    #+#              #
#    Updated: 2019/07/28 06:53:50 by kbelov           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

#FROM ruby
#RUN apt-get update -y && apt-get upgrade -y
#RUN gem install rails
#ONBUILD COPY . /opt/app
#ONBUILD WORKDIR /opt/app
#ONBUILD RUN bundle install
#ONBUILD RUN rails db:migrate
#ONBUILD RUN rails db:seed

FROM ruby

#MAINTAINER bogoncha "bogoncha@student.42.us.org"

RUN apt-get update -y && apt-get install -y build-essential libpq-dev nodejs sqlite3

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD EXPOSE 3000
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed

# update and install rails
# docker build -t ex02 .
