# WordPress + Elasticsearch + Kibana + Beats
Environment of WordPress, ELK and Beats using Docker.

## Usage

### start container
Start container with ``docker-compose.yml``

```
$ docker-compose up
```

show browser at ``localhost:8080`` .

### stop container

```
$ docker-compose stop

or 

$ ctrl + c  // force stop
```

### create index template

```
$ curl -H 'Content-Type: application/json' -XPUT 'http://localhost:9200/_template/packetbeat' -d@packetbeat.template.json
```

when creation success, return ``{“acknowledged":true}``.

To check the index.

```
$ curl "localhost:9200/_template/packetbeat?pretty"``
```

