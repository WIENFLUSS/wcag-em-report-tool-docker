FROM starefossen/ruby-node:2-10

MAINTAINER Christian Ebner <ebner@wienfluss.net>

# install compass
RUN gem install compass
RUN npm install -g bower grunt http-server

#COPY ./wcag-em-report-tool /tool
#ADD ./wcag-em-report-tool ./tool
RUN mkdir /tool

RUN git clone https://github.com/wienfluss/wcag-em-report-tool.git /tool

WORKDIR /tool

RUN npm install
RUN npx bower install --allow-root
RUN npm run build

WORKDIR /tool/dist

ENTRYPOINT [ "hs", "-p 9000" ]