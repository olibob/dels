## Elasticsearch + Kibana + sense plugin

Quick docker setup to get [elasticsearch](https://hub.docker.com/_/elasticsearch/) (stable 2 version) and [kibana](https://hub.docker.com/_/kibana/) with the [sense plugin](https://github.com/elastic/sense) up and running.

This has been tested on Docker for Mac  1.12.0-rc2.

## Cluster sertup

The cluster has 2 nodes: els1 (master) and els2.

### Configuration

Configuration for the elasticsearch nodes are located in `config-els1` and `config-els2` folders
els1 is forced as master.

## Access URLs

Both kibana and elasticsearch run on standard ports. Replace `localhost` with your VM IP or mapped host name if needed.

### els1 (master)

Although not needed, els1 can be accessed directly on http://localhost:9200.

### kibana

Access kibana at http://localhost:5601.

### Sense

Access sense at http://localhost:5601/app/sense.

When using the sense plugin: the elasticsearch server is located at http://els1:9200.

![alt text](https://raw.githubusercontent.com/olibob/dels/master/docs/sense.png)

### Marvel

A demo of Marvel is valid for 30 days to give it a run. It can be accessed from within kibana or directly at http://localhost:5601/app/marvel.

Give it a shot to check shards allocation, replication, metrics, ...

## Usage

`cd` into the base directory and ...

```
docker network create mynet
docker-compose up
```
