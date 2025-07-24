# Logstash with Opensearch

This repository hosts a custom Docker image that integrates **Logstash** with **OpenSearch** for seamless log ingestion and processing.

## 🧰 Features

- Preconfigured Logstash with OpenSearch output plugin
- Compatible with OpenSearch ≥ 2.x
- Suitable for local dev and production pipelines

## 📦 Image Location

The Docker image is available on

```
docker pull ghcr.io/mfzhsn/logstash-opensearch/logstash-with-opensearch:8.14.0
```

## Build Locally yourself

**Step-1**: Create a file called `Dockerfile`

```
FROM docker.elastic.co/logstash/logstash:8.14.0

# Install the OpenSearch output plugin
RUN logstash-plugin install logstash-output-opensearch
```

**Step-2**: Build the image

```
docker build -t logstash-opensearch .
```

More details on the Opensearch Link:  https://docs.opensearch.org/docs/latest/tools/logstash/index/#docker
