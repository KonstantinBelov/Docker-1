FROM ubuntu

RUN apt-get update && apt-get install -y cowsay fortune lolcat

ENTRYPOINT /usr/games/fortune | /usr/games/cowsay | /usr/games/lolcat

# To build:
# docker build -t a01 .

# To run:
# docker run --rm -ti a01
