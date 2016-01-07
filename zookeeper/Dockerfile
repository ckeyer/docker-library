FROM ckeyer/java:8-jre

MAINTAINER "ckeyer" <docker@ckeyer.com>

# Install zookeeper
ENV ZOOKEEPER_VERSION zookeeper-3.4.7
ENV ZOO_DIR /usr/local/zookeeper
RUN curl -Ss "http://apache.fayea.com/zookeeper/zookeeper-3.4.7/$ZOOKEEPER_VERSION.tar.gz" | tar xzf - -C /usr/local/ && \
	mv /usr/local/$ZOOKEEPER_VERSION $ZOO_DIR && \
	cp $ZOO_DIR/conf/zoo_sample.cfg $ZOO_DIR/conf/zoo.cfg

ENV PATH=$PATH:$ZOO_DIR/bin

EXPOSE 2181

CMD ["zkServer.sh", "start-foreground"]

