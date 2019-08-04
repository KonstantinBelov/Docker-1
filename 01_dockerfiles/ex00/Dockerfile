# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: kbelov <marvin@42.fr>                      +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/07/27 08:24:20 by kbelov            #+#    #+#              #
#    Updated: 2019/07/27 22:34:42 by kbelov           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM alpine

RUN apk update && apk upgrade && apk add vim

CMD	["vim"]

# to build:
# docker build -t ex00 .

# to run interactively, delete the container on exit:
# docker run --rm -ti ex00
