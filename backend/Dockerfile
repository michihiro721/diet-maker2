FROM ruby:3.3.6

RUN apt-get update -qq && apt-get install -y nodejs postgresql-client

WORKDIR /app

COPY Gemfile /app/Gemfile
COPY Gemfile.lock /app/Gemfile.lock

RUN gem install bundler:2.6.2
RUN bundle install

COPY . /app

CMD ["rails", "server", "-b", "0.0.0.0"]