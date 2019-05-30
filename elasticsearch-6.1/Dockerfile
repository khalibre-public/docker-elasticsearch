FROM docker.elastic.co/elasticsearch/elasticsearch:6.1.4
LABEL maintainer="Sida Say <sida.say@khalibre.com>"

RUN yum update -y \
	&& yum clean all \
	&& bin/elasticsearch-plugin install --batch analysis-kuromoji \
	&& bin/elasticsearch-plugin install --batch analysis-icu \
	&& bin/elasticsearch-plugin install --batch analysis-smartcn \
  && bin/elasticsearch-plugin install --batch analysis-stempel \
	&& rm -rf rm -rf /var/cache/yum/* /tmp/* /var/tmp/*
