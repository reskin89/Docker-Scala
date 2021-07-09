FROM adoptopenjdk/openjdk15:alpine

RUN apk add --no-cache --virtual=.build-dependencies wget ca-certificates && \
	apk add --no-cache bash curl jq && \
	curl -fLo coursier https://git.io/coursier-cli  &&\
	chmod +x coursier &&\
	mv coursier /usr/bin/coursier &&\
	coursier install scala3-compiler &&\
	coursier install scala3-repl

ENV PATH="${PATH}:/root/.local/share/coursier/bin"
