## Elasticsearch + Kibana + sense plugin

Quick docker setup to get [elasticsearch](https://hub.docker.com/_/elasticsearch/) (stable 2 version) and [kibana](https://hub.docker.com/_/kibana/) with the [sense plugin](https://github.com/elastic/sense) up and running.

This has been tested on Docker for Mac  1.12.0-rc2.

## Access URLs

Both kibana and elasticsearch run on the standard ports. Replace `localhost` with your HyperV VM IP or mapped host name on Windows.

### kibana

Access kibana at http://localhost:5601.

### Sense

Access sense at http://localhost:5601/app/sense.

When using the sense plugin: the elasticsearch server is located at http://elasticsearch:9200.

![alt text](https://raw.githubusercontent.com/olibob/dels/master/docs/sense.png)

### Marvel

A demo of Marvel is valid for 30 days to give it a run. It can be accessed from within kibana or directly at http://localhost:5601/app/marvel.
