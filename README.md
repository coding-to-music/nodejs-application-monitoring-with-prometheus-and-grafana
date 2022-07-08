# nodejs-application-monitoring-with-prometheus-and-grafana

## Node.js Application Monitoring with Prometheus and Grafana

Node.js Application Monitoring with Prometheus and Grafana

Application monitoring is essential for every production software system. In this article, we get to know Prometheus and Grafana and learn how to use them to monitor Node.js applications.

By Kentaro Wakayama https://codersociety.com/blog/articles/nodejs-application-monitoring-with-prometheus-and-grafana

15 September 2020 - 4 min read

# 🚀 Node.js Application Monitoring with Prometheus and Grafana 🚀

https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana

From / By https://github.com/coder-society/nodejs-application-monitoring-with-prometheus-and-grafana

![](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/nodejs-performance-monitoring-with-prometheus-and-grafana.png?raw=true)

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

# The RED Method: How to Instrument Your Services

https://grafana.com/blog/2018/08/02/the-red-method-how-to-instrument-your-services/

Julie Dam https://grafana.com/author/jdam/

• 2 Aug 2018 • 4 min read

![Tom Wilkie - Grafana Labs](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/tom_wilkie.jpg?raw=true)

Tom Wilkie - Grafana Labs

At GrafanaCon EU in March, we had the pleasure of introducing one of Grafana Labs’ newest team members, Tom Wilkie, who joined as VP, Product with the acquisition of Kausal.

And he came bearing gifts: his popular talk about the RED Method of monitoring microservices, which he created in 2015.

## The USE Method

In the talk, Tom first went over the USE Method of instrumenting, which has been popularized by Brendan Gregg:

For every resource, monitor:

- Utilization (% time that the resource was busy)
- Saturation (amount of work resource has to do, often queue length)
- Errors (count of error events)

“It’s a way of building a checklist that goes through everything,” he said. “It helps you know what you don’t know.” But he pointed out that this method, while useful, is somewhat abstract. Applying it to memory, for instance, is hard. “Memory utilization is tricky. What is it? Do you count caches toward utilization?” he said. “Saturation of memory is kind of a weird one… And what is a memory error? And how do you count them in Linux?”

## The RED Method

Tom then turned to his RED Method, which he created after a new employee asked what his monitoring philosophy was. “The USE Method doesn’t really apply to services; it applies to hardware, network disks, things like this,” Tom said. “We really wanted a microservices-oriented monitoring philosophy, so we came up with the RED Method.”

For every resource, monitor:

- Rate (the number of requests per second)
- Errors (the number of those requests that are failing)
- Duration (the amount of time those requests take)

- (See his presentation slides on the Prometheus implementation of the RED Method) https://grafana.com/files/grafanacon_eu_2018/Tom_Wilkie_GrafanaCon_EU_2018.pdf

“Everyone should understand the error rate, the request rate, and then some distribution of latency for those requests,” Tom explained.

“You model this for every single service in your architecture, and this gives you a nice, consistent view of how your architecture is behaving. Giving this kind of consistency across services allows you to scale your operational team, and allows you to put people on call for code they didn’t write.”

Plus, he pointed out, “The RED Method is a good proxy to how happy your customers will be. If you’ve got a high error rate, that’s basically going through to your users and they’re getting page load errors. If you’ve got a high duration, your website is slow. So these are really good metrics for building meaningful alerts and measuring your SLA.”

## The Four Golden Signals

Finally, Tom looked at a third method: The Four Golden Signals, which is from Google’s SRE book. https://landing.google.com/sre/book.html

For each service, monitor:

- Latency (time taken to serve a request)
- Traffic (how much demand is placed on your system)
- Errors (rate of requests that are failing)
- Saturation (how “full” your service is)

This is basically the same as the RED Method, but includes saturation. He explained one approach to measuring saturation: “With kube-state-metrics, a little job you run on your Kubernetes cluster that scrapes the Kubernetes API and exports really interesting metadata about your jobs and services and pods and so on, you can compare the amount of CPU a service is using against its quota. Like how much it should be using, or how much is it allowed to use, as a proportion between 1 and 0. This gives you a measure of how ‘full’ your service is, or some proxy for how full your service is at least. And this is super useful because you could for instance build an alert on this.”

## Two Sides of the Same Coin

Tom recommended using the USE and RED Methods together. “It’s like the RED Method is about caring about your users and how happy they are,” Tom said, “and the USE Method is about caring about your machines and how happy they are. It’s really just two different views on the same system. They’re complimentary.”

Watch Tom’s full talk in the video below.

Video: The RED Method: How to Instrument Your Services https://www.youtube.com/watch?v=zk77VS98Em8&feature=emb_imp_woyt

# Node.js Application Monitoring with Prometheus and Grafana

Node.js Application Monitoring with Prometheus and Grafana

Application monitoring is essential for every production software system. In this article, we get to know Prometheus and Grafana and learn how to use them to monitor Node.js applications.

By Kentaro Wakayama https://codersociety.com/blog/articles/nodejs-application-monitoring-with-prometheus-and-grafana

15 September 2020 - 4 min read

![](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/nodejs-performance-monitoring-with-prometheus-and-grafana.png?raw=true)

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

```java
cd nodejs-monitoring-with-prometheus-and-grafana
```

Start the Docker containers:

```java
docker-compose up -d
```

## Test containers

- Prometheus should be accessible via [http://localhost:9090](http://localhost:9090)
- Grafana should be accessible via [http://localhost:3000](http://localhost:3000)
- Example Node.js server metrics for RED monitoring should be accessible via [http://localhost:8080/metrics](http://localhost:8080/metrics)

## Open monitoring dashboards

Open in your web browser the monitoring dashboards:

- Monitoring dashboard for the Node.js app can be found on[http://localhost:3000/d/1DYaynomMk/example-service-dashboard](http://localhost:3000/d/1DYaynomMk/example-service-dashboard)

## What is Prometheus and how does it work?

![](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/Performance-Monitoring-Table.png?raw=true)

Prometheus is an open-source monitoring system which was created in 2012 by Soundcloud. In 2016, Prometheus became the second project (following Kubernetes) to be hosted by the Cloud Native Computing Foundation.

## Performance Monitoring architecture diagram with Prometheus and Grafana

The Prometheus server collects metrics from your servers and other monitoring targets by pulling their metric endpoints over HTTP at a predefined time interval. For ephemeral and batch jobs, for which metrics can't be scraped periodically due to their short-lived nature, Prometheus offers a Pushgateway. This is an intermediate server that monitoring targets can push their metrics to before exiting. The data is retained there until the Prometheus server pulls it later.

The core data structure of Prometheus is the time series, which is essentially a list of timestamped values that are grouped by metric.

With PromQL (Prometheus Query Language), Prometheus provides a functional query language allowing for selection and aggregation of time series data in real time. The result of a query can be viewed directly in the Prometheus web UI, or consumed by external systems such as Grafana via the HTTP API.

## How to use prom-client to export metrics in Node.js for Prometheus?

prom-client is the most popular Prometheus client libary for Node.js. It provides the building blocks to export metrics to Prometheus via the pull and push methods and supports all Prometheus metric types such as histogram, summaries, gauges and counters.

## Setup sample Node.js project

Create a new directory and setup the Node.js project:

```java
mkdir example-nodejs-app
cd example-nodejs-app
npm init -y
```

## Install prom-client

The prom-client npm module can be installed via:

```java
npm install prom-client
```

## Exposing default metrics

Every Prometheus client library comes with predefined default metrics that are assumed to be good for all applications on the specific runtime. The prom-client library also follows this convention. The default metrics are useful for monitoring the usage of resources such as memory and CPU.

You can capture and expose the default metrics with following code snippet:

```java
const http = require('http')
const url = require('url')
const client = require('prom-client')

// Create a Registry which registers the metrics
const register = new client.Registry()

// Add a default label which is added to all metrics
register.setDefaultLabels({
  app: 'example-nodejs-app'
})

// Enable the collection of default metrics
client.collectDefaultMetrics({ register })

// Define the HTTP server
const server = http.createServer(async (req, res) => {
  // Retrieve route from request object
  const route = url.parse(req.url).pathname

  if (route === '/metrics') {
    // Return all metrics the Prometheus exposition format
    res.setHeader('Content-Type', register.contentType)
    res.end(register.metrics())
  }
})

// Start the HTTP server which exposes the metrics on http://localhost:8080/metrics
server.listen(8080)
Collapse code
Exposing custom metrics
While default metrics are a good starting point, at some point, you’ll need to define custom metrics in order to stay on top of things.

Capturing and exposing a custom metric for HTTP request durations might look like this:

const http = require('http')
const url = require('url')
const client = require('prom-client')

// Create a Registry which registers the metrics
const register = new client.Registry()

// Add a default label which is added to all metrics
register.setDefaultLabels({
  app: 'example-nodejs-app'
})

// Enable the collection of default metrics
client.collectDefaultMetrics({ register })

// Create a histogram metric
const httpRequestDurationMicroseconds = new client.Histogram({
  name: 'http_request_duration_seconds',
  help: 'Duration of HTTP requests in microseconds',
  labelNames: ['method', 'route', 'code'],
  buckets: [0.1, 0.3, 0.5, 0.7, 1, 3, 5, 7, 10]
})

// Register the histogram
register.registerMetric(httpRequestDurationMicroseconds)

// Define the HTTP server
const server = http.createServer(async (req, res) => {
    // Start the timer
  const end = httpRequestDurationMicroseconds.startTimer()

  // Retrieve route from request object
  const route = url.parse(req.url).pathname

  if (route === '/metrics') {
    // Return all metrics the Prometheus exposition format
    res.setHeader('Content-Type', register.contentType)
    res.end(register.metrics())
  }

  // End timer and add labels
  end({ route, code: res.statusCode, method: req.method })
})

// Start the HTTP server which exposes the metrics on http://localhost:8080/metrics
server.listen(8080)
```

Copy the above code into a file called server.js and start the Node.js HTTP server with following command:

```java
node server.js
```

You should now be able to access the metrics via http://localhost:8080/metrics.

How to scrape metrics from Prometheus
Prometheus is available as Docker image and can be configured via a YAML file.

Create a configuration file called prometheus.yml with following content:

```java
global:
  scrape_interval: 5s
scrape_configs:
  - job_name: "example-nodejs-app"
    static_configs:
      - targets: ["docker.for.mac.host.internal:8080"]
```

The config file tells Prometheus to scrape all targets every 5 seconds. The targets are defined under scrape_configs. On Mac, you need to use docker.for.mac.host.internal as host, so that the Prometheus Docker container can scrape the metrics of the local Node.js HTTP server. On Windows, use docker.for.win.localhost and for Linux use localhost.

Use the docker run command to start the Prometheus Docker container and mount the configuration file (prometheus.yml):

```java
docker run --rm -p 9090:9090 \
  -v `pwd`/prometheus.yml:/etc/prometheus/prometheus.yml \
  prom/prometheus:v2.20.1
```

Windows users need to replace pwd with the path to their current working directory.

You should now be able to access the Prometheus Web UI on http://localhost:9090

![](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/prometheus-web-ui.png?raw=true)

Prometheus Web UI screenshot

## What is Grafana and how does it work?

Grafana is a web application that allows you to visualize data sources. A visualization can be a graph or chart. It comes with a variety of chart types, allowing you to choose whatever fits your monitoring data needs. Multiple charts are grouped into dashboards in Grafana, so that multiple metrics can be viewed at once.

The metrics displayed in the Grafana charts come from data sources. Prometheus is one of the supported data sources for Grafana, but it can also use other systems, like AWS CloudWatch, or Azure Monitor.

Grafana also allows you to define alerts that will be triggered if certain issues arise, meaning you’ll receive an email notification if something goes wrong. For a more advanced alerting setup checkout the Grafana integration for Opsgenie.

Grafana Play Web UI screenshot showing Home

![](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/Grafana.png?raw=true)

## Starting Grafana

Grafana is also available as Docker container. Grafana datasources can be configured via a configuration file.

## Create a configuration file called datasources.yml with following content:

```java
apiVersion: 1

datasources:
  - name: Prometheus
    type: prometheus
    access: proxy
    orgId: 1
    url: http://docker.for.mac.host.internal:9090
    basicAuth: false
    isDefault: true
    editable: true
```

The configuration file specifies Prometheus as a datasource for Grafana. Please note that on Mac, we need to use docker.for.mac.host.internal as host, so that Grafana can access Prometheus. On Windows, use docker.for.win.localhost and for Linux use localhost.

Use the following command to start a Grafana Docker container and to mount the configuration file of the datasources (datasources.yml). We also pass some environment variables to disable the login form and to allow anonymous access to Grafana:

```java
docker run --rm -p 3000:3000 \
  -e GF_AUTH_DISABLE_LOGIN_FORM=true \
  -e GF_AUTH_ANONYMOUS_ENABLED=true \
  -e GF_AUTH_ANONYMOUS_ORG_ROLE=Admin \
  -v `pwd`/datasources.yml:/etc/grafana/provisioning/datasources/datasources.yml \
  grafana/grafana:7.1.5
```

Windows users need to replace pwd with the path to their current working directory.

You should now be able to access the Grafana Web UI on http://localhost:3000

![](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/grafana-web-ui.png?raw=true)

Grafana Web UI screenshot showing Home

## Configuring a Grafana Dashboard

Once the metrics are available in Prometheus, we want to view them in Grafana. This requires creating a dashboard and adding panels to that dashboard:

- Go to the Grafana UI at http://localhost:3000, click the + button on the left, and select Dashboard.
- In the new dashboard, click on the Add new panel button.
- In the Edit panel view, you can select a metric and configure a chart for it.
- The Metrics drop-down on the bottom left allows you to choose from the available metrics. Let’s use one of the default metrics for this example.
- Type process_resident_memory_bytes into the Metrics input and {{app}} into the Legend input.
- On the right panel, enter Memory Usage for the Panel title.
- As the unit of the metric is in bytes we need to select bytes(Metric) for the left y axis in the Axes section, so that the chart is easy to read for humans.
- You should now see a chart showing the memory usage of the Node.js HTTP server.

![](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/grafana-dashboard.png?raw=true)

Grafana Web UI showing editing of panel Metrics

Press Apply to save the panel. Back on the dashboard, click the small "save" symbol at the top right, a pop-up will appear allowing you to save your newly created dashboard for later use.

## Setting up alerts in Grafana

Since nobody wants to sit in front of Grafana all day watching and waiting to see if things go wrong, Grafana allows you to define alerts. These alerts regularly check whether a metric adheres to a specific rule, for example, whether the errors per second have exceeded a specific value.

Alerts can be set up for every panel in your dashboards.

Go into the Grafana dasboard we just created.

- Click on a panel title and select edit.
- Once in the edit view, select "Alerts" from the middle tabs, and press the Create Alert button.
- In the Conditions section specify 42000000 after IS ABOVE. This tells Grafana to trigger an alert when - the Node.js HTTP server consumes more than 42 MB Memory.
- Save the alert by pressing the Apply button in the top right.

![](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/grafana-alerting-setup.png?raw=true)

## Sample code repository

We created a code repository which contains a collection of Docker containers with Prometheus, Grafana, and a Node.js sample application. It also contains a Grafana dashboard, which follows the RED monitoring methodology.

Clone the repository:

```
git clone https://github.com/coder-society/nodejs-application-monitoring-with-prometheus-and-grafana.git
```

The JavaScript code of the Node.js app is located in the /example-nodejs-app directory. All containers can be started conveniently with docker-compose. Run the following command in the project root directory:

```java
# detached mode

docker-compose up -d

# view the logs as they happen

docker-compose up
```

After executing the command, a Node.js app, Grafana, and Prometheus will be running in the background. The charts of the gathered metrics can be accessed and viewed via the Grafana UI at http://localhost:3000/d/1DYaynomMk/example-service-dashboard.

![](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/grafana-example-service-dashboard.png?raw=true)

To generate traffic for the Node.js app, we will use the ApacheBench command line tool, which allows sending requests from the command line.

On MacOS, it comes pre-installed by default. On Debian-based Linux distributions, ApacheBench can be installed with the following command:

```java
sudo apt-get install apache2-utils
```

For Windows, you can download the binaries from Apache Lounge as a ZIP archive. ApacheBench will be named ab.exe in that archive.

This CLI command will run ApacheBench so that it sends 10,000 requests to the /order endpoint of the Node.js app:

https://codersociety.com/blog/articles/nodejs-application-monitoring-with-prometheus-and-grafana

```java
ab -m POST -n 10000 -c 100 http://localhost:8080/order
```

Output:

```java
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

Depending on your hardware, running this command may take some time.

After running the ab command, you can access the Grafana dashboard via http://localhost:3000/d/1DYaynomMk/example-service-dashboard.

![Figure 1: Requests per minute graph](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/grafana-request-rate.png?raw=true)

Figure 1: Requests per minute graph

Figure 1 shows that the Node.js app was handling ~1,500 requests per minute.

![Figure 2: Request errors per minute graph](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/grafana-request-errors.png?raw=true)

Figure 2: Request errors per minute graph

Figure 2 shows that there are a maximum of 20 errors per minute.

![](https://github.com/coding-to-music/nodejs-application-monitoring-with-prometheus-and-grafana/blob/main/images/grafana-request-duration.png?raw=true)

Figure 3: Request duration graph

Figure 3 shows the time it took to process a request. Displayed here are the 90th percentile, the median, and the average durations for different endpoints of the Node.js app. The 90th percentile is the slowest 10% of requests. For the 10,000 requests we sent with ApacheBench, this means the 1,000 requests that took the longest time. In this case, it shows that 1,000 requests to the /order endpoint took over 6 seconds.

## Summary

Prometheus is a powerful open-source tool for self-hosted monitoring. It’s a good option for cases in which you don’t want to build from scratch but also don’t want to invest in a SaaS solution.

With a community-supported client library for Node.js and numerous client libraries for other languages, the monitoring of all your systems can be bundled into one place.

Its integration is straightforward, involving just a few lines of code. It can be done directly for long-running services or with help of a push server for short-lived jobs and FaaS-based implementations.

Grafana is also an open-source tool that integrates well with Prometheus. Among the many benefits it offers are flexible configuration, dashboards that allow you to visualize any relevant metric, and alerts to notify of any anomalous behavior.

These two tools combined offer a straightforward way to get insights into your systems. Prometheus offers huge flexibility in terms of metrics gathered and Grafana offers many different graphs to display these metrics. Prometheus and Grafana also integrate so well with each other that it’s surprising they’re not part of one product.

You should now have a good understanding of Prometheus and Grafana and how to make use of them to monitor your Node.js projects in order to gain more insights and confidence of your software deployments.
