FROM fluent/fluentd:v1.5-1

# Use root account to use apk
USER root

RUN  apk add --no-cache --update geoip-dev \
    && apk add --no-cache --update --virtual .build-deps build-base ruby-dev \
    && echo 'gem: --no-document' >> /etc/gemrc \
    && gem install fluent-plugin-elasticsearch fluent-plugin-woothee fluent-plugin-ua-parser fluent-plugin-geoip-filter fluent-plugin-multi-format-parser \
    && gem sources --clear-all \
    && apk del .build-deps \
    && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem

COPY fluent.conf /fluentd/etc/
COPY entrypoint.sh /bin/

ENV FLUENT_UID=0
#USER fluent