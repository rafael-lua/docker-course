FROM openjdk:8

WORKDIR /usr/src/app

COPY . .

RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]

# Commands used:
# -> docker build . -t 'java-spring'
# -> docker run -p 127.0.0.1:8080:8080 java-spring
