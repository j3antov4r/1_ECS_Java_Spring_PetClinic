FROM frolvlad/alpine-oraclejdk8-temporary:slim
ARG JAR_FILE
ARG JAR_PATH
VOLUME /tmp
COPY ${JAR_FILE} app.jar
RUN sh -c 'touch /app.jar'
ENV JAVA_OPTS=""
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar" ]

