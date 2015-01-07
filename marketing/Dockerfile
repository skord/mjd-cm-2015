FROM ruby:2.1
RUN apt-get update -qq &&\
            apt-get install -y build-essential libpq-dev nodejs &&\
            mkdir /opt/app/marketing
WORKDIR /opt/app/marketing
COPY Gemfile /opt/app/marketing/Gemfile
COPY Gemfile.lock /opt/app/marketing/Gemfile.lock
RUN bundle install --deployment
COPY . /opt/app/marketing
