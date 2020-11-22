FROM ubuntu
FROM ruby:2.6.0

RUN apt-get update && apt-get install -y nodejs

COPY . /app
WORKDIR /app

RUN gem install bundler
RUN bundle install

RUN rails db:migrate

EXPOSE 3000

ENTRYPOINT ["rails", "s"]
