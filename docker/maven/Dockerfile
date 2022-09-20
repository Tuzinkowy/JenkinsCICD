FROM maven:3.8.6-openjdk-8
COPY thumbnailer thumbnailer
WORKDIR /thumbnailer/imageio-extensions
RUN mvn verify
RUN mvn install
WORKDIR /thumbnailer/app
RUN mvn verify
RUN mvn install
RUN mv thumbnail.sh /thumbnailer/app/target
WORKDIR /thumbnailer/app/target
EXPOSE 8888
ENTRYPOINT [ "/thumbnailer/app/target/thumbnail.sh" ]