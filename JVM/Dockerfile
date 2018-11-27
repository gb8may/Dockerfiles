FROM java:8

MAINTAINER Mayara Gouveia "mayara.gouveia@ifactory.com.br"

VOLUME /tmp
EXPOSE 8080

ENV APP_HOME /root/PROD/mobigo/target/
ENV SPRING_PROFILES_ACTIVE prod

RUN cd $APP_HOME

ADD MobiGo.war $APP_HOME/MobiGo.war

WORKDIR $APP_HOME
RUN java -jar MobiGo.war

ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar"]
