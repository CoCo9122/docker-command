FROM openjdk:18-alpine

ARG JAR_FILE=target

WORKDIR /usr/app

COPY ./../spring-boot-docker /

CMD ["./mvnw", "clean", "spring-boot:run"]

# 