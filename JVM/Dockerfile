FROM java:8

MAINTAINER Mayara Gouveia "mayara.gouveia@ifactory.com.br"

VOLUME /tmp
EXPOSE 8080

ENV APP_HOME /root/PROD/mobigo/target/
ENV JPA_SHOW_SQL false
ENV JWT_EXPIRATION_IN_MS 604800000
ENV JWT_SECRET secret
ENV SPRING_PROFILES_ACTIVE qa

RUN cd $APP_HOME

ADD MobiGo.war $APP_HOME/MobiGo.warr

WORKDIR $APP_HOME
RUN java $JAVA_OPTS -Dserver.port=$PORT -jar *.war

ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","jvm-bloggers.jar"]
