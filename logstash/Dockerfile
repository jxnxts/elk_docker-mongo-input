ARG ELASTIC_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/logstash/logstash:${ELASTIC_VERSION}

# Set user to root
USER root

RUN apt install netbase -y

# Add your logstash plugins setup here
RUN logstash-plugin install logstash-input-mongodb

# Create directory for SQLite Database
RUN mkdir -p /opt/logstash-mongodb/