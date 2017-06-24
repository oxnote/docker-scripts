FROM alpine:3.6

RUN apk update; \
    apk add curl; \
    curl https://raw.githubusercontent.com/oxnote/docker-scripts/master/ruby/install-2.4.1 | sh

ENV GEM_HOME="/usr/local/bundle" \
    BUNDLE_PATH="$GEM_HOME" \
	BUNDLE_BIN="$GEM_HOME/bin" \
	BUNDLE_SILENCE_ROOT_WARNING=1 \
	BUNDLE_APP_CONFIG="$GEM_HOME" \
    PATH $BUNDLE_BIN:$PATH

CMD [ "irb" ]
