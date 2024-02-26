FROM maven:3.8.4-jdk-11-slim as builder
WORKDIR /build

COPY . .
RUN mvn dependency:resolve && mvn package

FROM openjdk:11-jre-slim

ARG jar_file=worker-jar-with-dependencies.jar
ARG work_dir=app
WORKDIR /${work_dir}

COPY --from=builder build/target/${jar_file} ./${jar_file}
CMD ["java", "-jar", "./${jar_file}"]
