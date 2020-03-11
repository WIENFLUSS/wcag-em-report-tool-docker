FROM starefossen/ruby-node:2-10

MAINTAINER Christian Ebner <ebner@wienfluss.net>

# install compass
RUN gem install compass
RUN npm install -g bower grunt http-server

# create directory to host the WCAG-EM tool
RUN mkdir /tool

# initialize optional argutments
ARG GITURL="https://github.com/w3c/wcag-em-report-tool.git"
ARG GITBRANCH=""

# Clone the WCAG-EM tool. Either default or a given GIT repository.
RUN git clone $GITURL /tool

WORKDIR /tool

# If GITBRANCH is supplied as an argument, checkout the named branch
RUN test -z "$GITBRANCH" || git checkout $GITBRANCH && :

# install npm and build the tool
RUN npm install
RUN npx bower install --allow-root
RUN npm run build

WORKDIR /tool/dist

ENTRYPOINT [ "hs", "-p 9000" ]