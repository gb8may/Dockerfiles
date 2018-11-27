FROM java:8

MAINTAINER Mayara Gouveia "mayara.gouveia@ifactory.com.br"

VOLUME /tmp
EXPOSE 8080

ENV SPRING_PROFILES_ACTIVE qa
ENV USER_NAME user
ENV APP_HOME /home/$USER_NAME/app

RUN useradd -ms /bin/bash $USER_NAME
RUN mkdir $APP_HOME

ADD target/MobiGo.war $APP_HOME/MobiGo.war
RUN chown $USER_NAME $APP_HOME/MobiGo.war

USER $USER_NAME
WORKDIR $APP_HOME
RUN bash -c 'touch MobiGo.war'

ENTRYPOINT ["java","-jar","MobiGo.war"]
