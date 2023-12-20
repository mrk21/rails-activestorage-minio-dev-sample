FROM ruby:3.2.2
ENV LANG C.UTF-8
ENV DEBIAN_FRONTEND noninteractive

# Install basic packages
RUN apt-get update -qq && \
    apt-get install -y build-essential tree vim less dnsutils net-tools && \
    apt-get install -y --no-install-recommends apt-utils

# Install MySQL client
RUN apt-get install -y default-mysql-client

# Install ActiveStorage dependencies
RUN apt-get install -y --no-install-recommends libvips42

# Install bundler
RUN gem install bundler

ENV APP_HOME /app
RUN mkdir -p $APP_HOME
WORKDIR $APP_HOME
