FROM alpine:latest

RUN apk update
RUN apk fetch openjdk8
RUN apk add openjdk8
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
ENV PATH="$JAVA_HOME/bin:${PATH}"
COPY . .
RUN javac -cp "kafka/installation/kafka_files/libs/*" kafka/project4/ProduceMessage.java
CMD java -cp "kafka/installation/kafka_files/libs/*":. kafka/project4/ProduceMessage