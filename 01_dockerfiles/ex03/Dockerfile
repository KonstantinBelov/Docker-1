# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: kbelov <marvin@42.fr>                      +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/07/28 06:57:25 by kbelov            #+#    #+#              #
#    Updated: 2019/07/29 08:40:52 by kbelov           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y ca-certificates openssh-server wget postfix

RUN wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh && \
	chmod 777 script.deb.sh && ./script.deb.sh && apt-get install -y gitlab-ce

RUN apt update && apt install -y tzdata && \
	apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

EXPOSE 443 80 22

ENTRYPOINT (/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure && tail -f /dev/null

# To build:
# docker build -t ex03 .

# To run:
# docker run -it --rm -p 8080:80 -p 8022:22 -p 8443:443 --privileged ex03

# To reset:
# docker rm -f $(docker ps -a -q)
# docker rmi $(docker images -a -q)
