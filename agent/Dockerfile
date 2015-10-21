FROM java:8-jre

RUN cd /tmp && \
    wget http://download.jetbrains.com/teamcity/TeamCity-9.1.3.tar.gz && \
    cd /opt/ && tar xf /tmp/TeamCity-9.1.3.tar.gz && \
    rm /tmp/TeamCity*

COPY buildAgent.properties /opt/TeamCity/buildAgent/conf/buildAgent.properties
CMD ["/opt/TeamCity/buildAgent/bin/agent.sh", "run"]
