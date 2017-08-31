FROM circleci/node:6.11

USER root

# delete node 6.11 files
RUN rm -f /usr/local/bin/node /usr/local/bin/nodejs /usr/local/bin/npm /usr/local/share/man/man1/node.1 /usr/local/share/systemtap/tapset/node.stp
RUN rm -rf /usr/local/lib/node_modules /usr/local/include/node /usr/local/share/doc/node

# download node 6.8.1 from here: https://nodejs.org/en/download/releases
RUN wget https://nodejs.org/download/release/v6.8.1/node-v6.8.1.tar.gz
RUN tar xvf node-v6.8.1.tar.gz

WORKDIR node-v6.8.1

# install node 6.8.1 as described here: https://github.com/nodejs/node/blob/master/BUILDING.md#building-nodejs-on-supported-platforms
RUN ./configure
RUN make -j4
RUN make doc
RUN make install

USER circleci