FROM java:8-jre

RUN cd /tmp && \
    wget http://download.jetbrains.com/teamcity/TeamCity-9.1.3.tar.gz && \
    cd /opt/ && tar xf /tmp/TeamCity-9.1.3.tar.gz && \
    rm /tmp/TeamCity*

ENV TEAMCITY_DATA_PATH /var/lib/TeamCity
EXPOSE 8111

CMD ["/opt/TeamCity/bin/teamcity-server.sh", "run"]
