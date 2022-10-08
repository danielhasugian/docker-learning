FROM adoptopenjdk/openjdk11 AS build-env
WORKDIR /source
COPY src .
RUN javac -verbose HelloWorld.java

FROM adoptopenjdk/openjdk11:jre-11.0.8_10-ubi-minimal
EXPOSE 80
WORKDIR /target
COPY --from=build-env /source/*.class ./
ENTRYPOINT ["java", "HelloWorld"]
