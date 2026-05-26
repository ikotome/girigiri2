FROM ruby:4.0-slim

RUN apt-get update -qq && \
    apt-get install -y --no-install-recommends \
    build-essential libpq-dev libyaml-dev git curl && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY Gemfile Gemfile.lock ./
RUN bundle install
