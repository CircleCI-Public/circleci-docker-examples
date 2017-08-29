FROM circleci/ruby:2.4.1-node-browsers

USER root

# install dependencies here so we don't have to install over & over again every time we run builds!
RUN apt-get update
RUN apt-get install -y qt5-default libqt5webkit5-dev gstreamer1.0-plugins-base gstreamer1.0-tools gstreamer1.0-x postgresql-client

USER circleci