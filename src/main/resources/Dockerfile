ARG REGISTRY
FROM halosee_jre8

MAINTAINER liujiang@haolosee.com

RUN mkdir -p /app/example

WORKDIR /app/example

EXPOSE 8086

ADD target/example-*.jar  ./app.jar

ENTRYPOINT ["java", "-Djava.security.egd=file:/dev/./urandom", "-Dfile.encoding=UTF-8", "-Dsun.jnu.encoding=UTF-8", "-jar", "app.jar"]

CMD ["--spring.profiles.active=dev"]
