# Elasticsearch, Logstash and Kibana, Metricbeat (ELKM) dockerized for testing

This repo contains ELKM stack as docker-compose file for getting started/testing ELKM with Docker.

This docker-compose file is for testing purposes only.

For configuring [logstash settings](https://www.elastic.co/guide/en/logstash/current/logstash-settings-file.html) modify `logstash.yml` currently the config is set to auto-reload and restart logstash gracefully upon modification/addition of logstash pipelines at `pipeline/*.conf`

There is a sample [logstash pipeline](https://www.elastic.co/guide/en/logstash/current/configuration.html) included in `pipelines/sample.conf` this logstash pipeline makes use of the [`heartbeat`](https://www.elastic.co/guide/en/logstash/current/plugins-inputs-heartbeat.html) input plugin to get started

## Getting started

* [Install Docker Compose](https://docs.docker.com/compose/install/)

* clone this repo `cd elkm-stack` and run `docker-compose up -d`

* head to <http://localhost:5601> to explore the data with Kibana

#### Metricbeat
* head to System Overview Dashboard <http://localhost:5601/app/kibana#/dashboard/Metricbeat-system-overview>
