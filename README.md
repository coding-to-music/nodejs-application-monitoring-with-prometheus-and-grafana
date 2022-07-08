# nodejs-application-monitoring-with-prometheus-and-grafana

# 🚀 Javascript full-stack 🚀

https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana

From / By https://github.com/coder-society/nodejs-application-monitoring-with-prometheus-and-grafana

![](https://cdn.codersociety.com/uploads/keystone/nodejs-performance-monitoring-with-prometheus-and-grafana.png)

We discuss this repository in this article in detail:
https://codersociety.com/blog/articles/nodejs-application-monitoring-with-prometheus-and-grafana

The repository contains a sample Node.js app which integrates the [Prometheus client for node.js](https://github.com/siimon/prom-client) and exposes metrics on [http://localhost:8080/metrics](http://localhost:8080/metrics). The metrics are periodically scraped by [Prometheus](https://prometheus.io) and visualized through a [Grafana](https://grafana.com/oss/grafana) monitoring dashboard.

## Prometheus port has been changed to 9095 to avoid conflicts with existing use of the port

Prometheus port has been changed to 9095 to avoid conflicts with existing use of the port

## Environment variables:

```java

```

## GitHub

```java
git init
git add .
git remote remove origin
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana.git
git push -u origin main
```

# Node.js Application Monitoring with Prometheus and Grafana

![](https://cdn.codersociety.com/uploads/keystone/nodejs-performance-monitoring-with-prometheus-and-grafana.png)

We discuss this repository in this article in detail:
https://codersociety.com/blog/articles/nodejs-application-monitoring-with-prometheus-and-grafana

The repository contains a sample Node.js app which integrates the [Prometheus client for node.js](https://github.com/siimon/prom-client) and exposes metrics on [http://localhost:8080/metrics](http://localhost:8080/metrics). The metrics are periodically scraped by [Prometheus](https://prometheus.io) and visualized through a [Grafana](https://grafana.com/oss/grafana) monitoring dashboard.

## Prerequisites

Make sure that you have Docker and Docker Compose installed:

- [Docker Engine](https://docs.docker.com/engine)
- [Docker Compose](https://docs.docker.com/compose)

## Getting started

Clone the repository:

```bash
git clone https://github.com/coder-society/nodejs-monitoring-with-prometheus-and-grafana.git
```

Navigate into the project directory:

```bash
cd nodejs-monitoring-with-prometheus-and-grafana
```

Start the Docker containers:

```bash
docker-compose up -d
```

## Test containers

- Prometheus should be accessible via [http://localhost:9090](http://localhost:9090)
- Grafana should be accessible via [http://localhost:3000](http://localhost:3000)
- Example Node.js server metrics for RED monitoring should be accessible via [http://localhost:8080/metrics](http://localhost:8080/metrics)

## Open monitoring dashboards

Open in your web browser the monitoring dashboards:

- Monitoring dashboard for the Node.js app can be found on[http://localhost:3000/d/1DYaynomMk/example-service-dashboard](http://localhost:3000/d/1DYaynomMk/example-service-dashboard)
