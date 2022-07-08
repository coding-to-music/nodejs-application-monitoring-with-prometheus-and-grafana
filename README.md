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

## Sample code repository

We created a code repository which contains a collection of Docker containers with Prometheus, Grafana, and a Node.js sample application. It also contains a Grafana dashboard, which follows the RED monitoring methodology.

Clone the repository:

```
git clone https://github.com/coder-society/nodejs-application-monitoring-with-prometheus-and-grafana.git
```

The JavaScript code of the Node.js app is located in the /example-nodejs-app directory. All containers can be started conveniently with docker-compose. Run the following command in the project root directory:

```
# detached mode
docker-compose up -d
# view the logs as they happen
docker-compose up
```

After executing the command, a Node.js app, Grafana, and Prometheus will be running in the background. The charts of the gathered metrics can be accessed and viewed via the Grafana UI at http://localhost:3000/d/1DYaynomMk/example-service-dashboard.

To generate traffic for the Node.js app, we will use the ApacheBench command line tool, which allows sending requests from the command line.

On MacOS, it comes pre-installed by default. On Debian-based Linux distributions, ApacheBench can be installed with the following command:

```
sudo apt-get install apache2-utils
```

For Windows, you can download the binaries from Apache Lounge as a ZIP archive. ApacheBench will be named ab.exe in that archive.

This CLI command will run ApacheBench so that it sends 10,000 requests to the /order endpoint of the Node.js app:

https://codersociety.com/blog/articles/nodejs-application-monitoring-with-prometheus-and-grafana

```
ab -m POST -n 10000 -c 100 http://localhost:8080/order
```

Output:

```
This is ApacheBench, Version 2.3 <$Revision: 1843412 $>
Copyright 1996 Adam Twiss, Zeus Technology Ltd, http://www.zeustech.net/
Licensed to The Apache Software Foundation, http://www.apache.org/

Benchmarking localhost (be patient)
Completed 1000 requests
Completed 2000 requests
Completed 3000 requests
Completed 4000 requests
Completed 5000 requests
Completed 6000 requests
Completed 7000 requests
Completed 8000 requests
Completed 9000 requests
Completed 10000 requests
Finished 10000 requests


Server Software:
Server Hostname:        localhost
Server Port:            8080

Document Path:          /order
Document Length:        26 bytes

Concurrency Level:      100
Time taken for tests:   406.205 seconds
Complete requests:      10000
Failed requests:        89
   (Connect: 0, Receive: 0, Length: 89, Exceptions: 0)
Non-2xx responses:      89
Total transferred:      1009377 bytes
HTML transferred:       257686 bytes
Requests per second:    24.62 [#/sec] (mean)
Time per request:       4062.049 [ms] (mean)
Time per request:       40.620 [ms] (mean, across all concurrent requests)
Transfer rate:          2.43 [Kbytes/sec] received

Connection Times (ms)
              min  mean[+/-sd] median   max
Connect:        0    0   0.3      0       6
Processing:     0 3979 898.0   4001    5082
Waiting:        0 3979 898.0   4001    5080
Total:          1 3980 898.0   4001    5086

Percentage of the requests served within a certain time (ms)
  50%   4001
  66%   4072
  75%   5001
  80%   5001
  90%   5002
  95%   5002
  98%   5004
  99%   5006
 100%   5086 (longest request)
```
