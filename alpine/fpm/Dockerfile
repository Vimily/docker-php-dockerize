FROM php:7.4-fpm-alpine

ENV DOCKERIZE_VERSION v0.6.1

RUN apk add wget bash && \
	wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
		&& tar -C /usr/local/bin -xzvf dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
		&& rm dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
		&& chmod 1777 /tmp

ENTRYPOINT ["dockerize"]
CMD ["--help"]
