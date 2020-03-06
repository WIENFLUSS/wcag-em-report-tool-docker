FROM starefossen/ruby-node:2-10

MAINTAINER Christian Ebner <ebner@wienfluss.net>

# install compass
RUN gem install compass
RUN npm install -g bower grunt http-server

RUN mkdir /tool

ARG GITURL="https://github.com/w3c/wcag-em-report-tool.git"

RUN git clone $GITURL /tool

WORKDIR /tool

RUN npm install
RUN npx bower install --allow-root
RUN npm run build

WORKDIR /tool/dist

ENTRYPOINT [ "hs", "-p 9000" ]