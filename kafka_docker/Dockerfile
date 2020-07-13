FROM alpine:latest
COPY . .
RUN apk update
RUN apk add --update bash
RUN apk fetch openjdk8
RUN apk add openjdk8
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
ENV PATH="$JAVA_HOME/bin:${PATH}"
CMD ["./kafka/installation/kafka_files/bin/kafka-server-start.sh" , "./kafka/installation/kafka_files/config/server.properties"]