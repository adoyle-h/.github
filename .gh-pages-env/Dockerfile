ARG RUBY_VERSION=2.7.7
FROM ruby:$RUBY_VERSION-alpine

WORKDIR /src/site

ARG APK_PROXY
ARG GEM_PROXY

RUN if [ -n "$APK_PROXY" ]; then \
  cp /etc/apk/repositories /etc/apk/repositories.bak && \
  sed -i "s|dl-cdn.alpinelinux.org|$APK_PROXY|g" /etc/apk/repositories ; \
  fi

RUN if [ -n "$GEM_PROXY" ]; then \
  bundle config mirror.https://rubygems.org "https://$GEM_PROXY";\
  fi

COPY ./.gh-pages-env/Gemfile /src/site/

# one step to exclude .build_deps from docker cache
RUN apk add --no-cache --virtual .build_deps \
  make build-base git && \
  bundle install --verbose && \
  apk del .build_deps

ENV LANG en_US.UTF-8
ENV LANGUAGE en_US.UTF-8
ENV LC_ALL en_US.UTF-8

ENTRYPOINT ["github-pages"]
CMD ["serve", "-H", "0.0.0.0", "-P", "4000", "-I", "--watch", "--verbose"]
