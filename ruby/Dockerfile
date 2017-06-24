FROM alpine:3.6

RUN set -xe; \
    apk update; \
    apk add curl; \
    curl https://raw.githubusercontent.com/oxnote/docker-scripts/master/ruby/inst-ruby | sh

ENV GEM_HOME /usr/local/bundle
ENV BUNDLE_PATH="$GEM_HOME" \
	BUNDLE_BIN="$GEM_HOME/bin" \
	BUNDLE_SILENCE_ROOT_WARNING=1 \
	BUNDLE_APP_CONFIG="$GEM_HOME"
ENV PATH $BUNDLE_BIN:$PATH

CMD [ "irb" ]
