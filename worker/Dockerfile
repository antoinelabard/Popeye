FROM maven:3.8.4-jdk-11-slim as builder

WORKDIR /build
COPY . /build

RUN mvn package

FROM openjdk:11-jre-slim

WORKDIR /app
COPY --from=builder /build/target/worker-jar-with-dependencies.jar .

EXPOSE 80

CMD ["java", "-jar", "worker-jar-with-dependencies.jar"]
