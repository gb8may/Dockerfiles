FROM java:8

MAINTAINER Mayara Gouveia "gb8may@gmail.com"

VOLUME /tmp
EXPOSE 8080

ENV SPRING_PROFILES_ACTIVE XX
ENV USER_NAME user
ENV APP_HOME /home/$USER_NAME/app

RUN useradd -ms /bin/bash $USER_NAME
RUN mkdir $APP_HOME

ADD target/XXX.war $APP_HOME/XXX.war
RUN chown $USER_NAME $APP_HOME/XXX.war

USER $USER_NAME
WORKDIR $APP_HOME
RUN bash -c 'touch XXX.war'

ENTRYPOINT ["java","-jar","-Dspring.profiles.active=production","XXX.war"]
