# How to run reviews service

## Prerequisite

* Java 8

```bash
/opt/ibm/wlp/bin/server run defaultServer
```

## How to run with Docker

```bash
# Build Docker Image for book-details service
docker build -t book-reviews .

# Run book-details service on port 8082
docker run -d -it --name reviews -p 8082:9080 -e ENABLE_RATINGS=true book-reviews
```

* Test with path `/reviews/1` and `/health`