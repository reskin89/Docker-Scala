FROM adoptopenjdk/openjdk15:alpine

RUN apk add --no-cache --virtual=.build-dependencies wget ca-certificates && \
	apk add --no-cache bash curl jq && \
	wget https://github.com/sbt/sbt/releases/download/v1.5.4/sbt-1.5.4.tgz -P /tmp/ &&\
	tar -zxvf /tmp/sbt-1.5.4.tgz &&\
	mv /tmp/sbt/bin/sbt /bin/sbt &&\
	chmod +x /bin/sbt
