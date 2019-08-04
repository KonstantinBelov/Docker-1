FROM debian

RUN apt-get update && apt-get upgrade -y && apt-get install -y nodejs npm git vim

RUN npm install yarn --global && npm install npm --global

# To build:
# docker build -t a00 .

# To run:
# docker run --rm -ti a00
