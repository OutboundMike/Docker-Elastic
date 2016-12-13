![el-stack-logo](https://raw.githubusercontent.com/blacktop/docker-elastic-stack/master/docs/img/el_stack_logo.png)

Elastic Stack Dockerfile
========================

### Dependencies

-	[gliderlabs/alpine:3.4](https://index.docker.io/_/gliderlabs/alpine/)
-	[openjdk8-jre](https://pkgs.alpinelinux.org/package/v3.4/community/x86_64/openjdk8-jre)
-	[Elasticsearch](https://www.elastic.co/products/elasticsearch)
-	[Logstash](https://www.elastic.co/products/logstash)
-	[Kibana](https://www.elastic.co/products/kibana)

### Getting Started

$ docker run -d --name elstack -p 80:80 -p 9200:9200 outboundmike/Docker-Elastic

##### Now Navigate To

-	With [Docker for Mac](https://docs.docker.com/engine/installation/mac/) : `http://localhost`
-	With [docker-machine](https://docs.docker.com/machine/) : `http://$(docker-machine ip)`
-	With [docker-engine](https://docker.github.io/engine/installation/) : `$(docker inspect -f '{{ .NetworkSettings.IPAddress }}' elstack)`


#### You can also use each part of the stack independently

-	[outboundmike/elasticsearch](https://github.com/blacktop/docker-elasticsearch-alpine)
-	[outboundmike/logstash](https://github.com/blacktop/docker-logstash-alpine)
-	[outboundmike/kibana](https://github.com/blacktop/docker-kibana-alpine)

### Documentation

-	[Add some demo data](docs/add-data.md)
-	[Enable SSL](docs/ssl.md)
-	[Change nginx password](docs/change-pass.md)
-	[Build a multi-node Elastic Stack cluster](docs/mutil-node.md)
