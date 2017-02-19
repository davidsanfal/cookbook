# Elasticsearch and Docker

- [elasticsearch dockerhub](https://hub.docker.com/_/elasticsearch/)
- [kibana dockerhub](https://hub.docker.com/_/elasticsearch/)

```sh
docker run --name elastic -v [ES_FOLDER_TO_SAVE]:/usr/share/elasticsearch/data -p 9200:9200 -d elasticsearch:5
docker run --name sense --link elastic:elasticsearch  -p 5601:5601 -d kibana:5
```

```sh
sudo sysctl -w vm.max_map_count=262144
```

```sh
docker run --name sense -e ELASTICSEARCH_URL=http://[ES_IP]:[ES_PORT] -p 5601:5601 -d kibana:5
```