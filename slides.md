---
theme: seriph
colorSchema: light
background: https://cover.sli.dev
title: Elasticsearch Presentation for BCC
hideInToc: true
info: |
  ## Elasticsearch Presentation for BCC
class: text-center
drawings:
  persist: true
transition: slide-left
mdc: true
overviewSnapshots: true
globalBottomPosition: "left"
exportFilename: "file"
download: true
---

# Achieving High Ovservability through Elastic Stack

Samidhya Sarker<br/>
Assistant Programmer<br/>
Bangladesh Computer Council


---
layout: default
hideInToc: true
image: https://cover.sli.dev
---


# Presentation Outline

<Toc columns=2 maxDepth=2 />


---
layout: quote
background: https://cover.sli.dev
---


# Observability
Observability refers to understanding a system through **observation**, and classifies the tools


---
layout: cover
background: https://cover.sli.dev
---


## Observability of Applications vs Observability of Systems



---
layout: default
image: https://cover.sli.dev
---

### Observability of Systems
- Concentrates on monitoring and analyzing the **underlying infrastructure** (e.g., servers, networks, containers) that applications rely on. It includes:
    - **Key Metrics**: CPU, memory, disk I/O, network throughput, container health, etc.
    - **Events**: Logs related to system-level changes or failures (e.g., kernel panics, node crashes).
    - **Topology**: Relationships and dependencies between system components, such as container orchestration with Kubernetes.
    - **Primary Tools**: Infrastructure monitoring tools like Prometheus, Grafana, Nagios, or Splunk.
    - **Use Case**: Diagnosing issues like high server load, network latency, or disk space exhaustion.

---
layout: default
---

### Observability of Applications
- Focuses on monitoring and understanding the behavior, performance, and health of **software applications**. It centers around:
  - **Key Metrics**: Response times, throughput, error rates, request volumes, etc.
  - **Tracing**: End-to-end visibility of user interactions, such as tracing a request through APIs, services, and databases.
  - **Logs**: Application-specific logs for debugging, capturing exceptions, or auditing actions.
  - **Primary Tools**: Application Performance Monitoring (APM) solutions like New Relic, Dynatrace, or Datadog.
  - **Use Case**: Troubleshooting issues like slow API responses, memory leaks, or application-level bugs.


---

### Overlap and Differences

- **Overlap**: Both share some concerns, such as logging and metrics, but differ in granularity and scope. They often feed into the same dashboards for holistic observability.
- **Differences**:
    - Applications observability is **user-centric**, focusing on service behavior and business logic.
    - Systems observability is **resource-centric**, focusing on the infrastructure and operational concerns.

To achieve comprehensive observability, combine both domains, ensuring both application performance and system health are monitored cohesively.


---
layout: two-cols-header
level: 2
---

## Roles

::left::
## Sysadmin
<img
    src="https://cdn-icons-png.flaticon.com/512/5322/5322018.png"
    alt="Image 1"
    style="width: 70%; padding:30px"
/>

::right::
## Developer
<img
    src="https://static.vecteezy.com/system/resources/previews/002/206/015/original/developer-working-icon-free-vector.jpg"
    alt="Image 2"
    style="width: 70%"
/>

---
layout: section
---

## Elastic Architecture

---
layout: default
---

### Ingestion of Logs

![Elastic Architecture](https://www.elastic.co/guide/en/fleet/master/images/agent-architecture.png)

---

### Fleet Server Architecture

![Elastic Architecture](https://www.elastic.co/guide/en/fleet/current/images/fleet-server-cloud-deployment.png)

---
layout: image-right
image: https://cover.sli.dev
---

### Beats Architecture

<img src="https://static-www.elastic.co/v3/assets/bltefdd0b53724fa2ce/bltf8ff84bb00690338/652569565679eb17f76df06e/Screenshot_2023-10-10_at_9.09.57_AM.png" alt="Elastic Architecture" style="width: 100%">

---
layout: cover
background: assets/Elasticsearch101-Picture_2.webp
---

# Systems Monitoring

---
layout: quote
---

## SRE Performance Monitoring

https://www.brendangregg.com/Slides/SREcon_2016_perf_checklists.pdf


---
layout: image
image: assets/SREcon_2016_perf_checklists_002.jpg
backgroundSize: 80% 100%
title: Checklist
hideInToc: true
---


---
layout: image-right
image: https://cover.sli.dev
---

## What to monitor

- Metrics
  - CPU
  - Memory
  - Disk
  - Network
- Logs
- Traces

---
layout: default
# backgroundSize: 80% 70%
---
## Inventory

<img
    src="./assets/Screenshot 2024-11-27 at 10.58.45 AM.png"
    alt="Image 2"
    style="display: block; margin: 0 auto; width: 70%"
/>


---
layout: section
---

## Log Ingestion (Demo)

---
layout: iframe
url: https://kibana.bcc-ca.gov.bd:8888/app/logs/stream?logView=(logViewId:default,type:log-view-reference)&flyoutOptions=(flyoutId:!n,flyoutVisibility:hidden,surroundingLogsId:!n)&logFilter=(filters:!(),query:(language:kuery,query:%27%27),refreshInterval:(pause:!f,value:5000),timeRange:(from:now-1d,to:now))&logPosition=(position:(tiebreaker:0,time:1732697617225))
hideInToc: true
---

## Log

---
layout: iframe
url: https://kibana.bcc-ca.gov.bd:8888/app/r/s/HH219
hideInToc: true
---

## Log2


---
layout: cover
background: assets/Elasticsearch101-Picture_2.webp
---


# Custom Dashboard for VMs

---
layout: section
---

## Single VMs


---
layout: iframe
url: https://kibana.bcc-ca.gov.bd:8888/app/r/s/q1XQD
hideInToc: true
---

## Dashboard iframe (single vm)

---
layout: section
---

## Multiple VMs

---
layout: iframe
url: https://kibana.bcc-ca.gov.bd:8888/app/r/s/WqdT6
hideInToc: true
---

## Multiple VMs





---
layout: cover
background: https://plus.unsplash.com/premium_photo-1661855036857-7855c8de519e?w=900&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MTN8fGhvcnNlfGVufDB8fDB8fHww
---


# Applications Performance Monitoring

---
layout: image-right
image: https://plus.unsplash.com/premium_photo-1668373587657-0211ba2b8805?q=80&w=3270&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---



## APM Tools

- Counters
- Profiling
- Tracing

---

### 1. Counters
- Real-time **metrics** tracking for **key performance indicators**
- Monitors system vitals like **requests/sec, error rates, and resource usage**
- Enables **threshold-based alerting** and trend analysis

### 2. Profiling
- Deep dive analysis of application runtime behavior
- **CPU, memory, and thread usage examination**
- Identifies performance bottlenecks and resource-intensive operations

### 3. Tracing
- End-to-end visibility of request flow through distributed systems
- Tracks latency across **service boundaries and components**
- Helps diagnose issues in microservices architectures

---

## Counters
These are like the gauges in your car's dashboard. They constantly measure and record specific metrics in your application:
- Request rates: How many users/calls your system handles per second
- Error rates: How often things go wrong (like 404s or 500s)
- Response times: How fast your system responds
- Resource usage: CPU, memory, disk space consumption
- Custom business metrics: Like number of orders processed

Counters are great for real-time monitoring and alerting. For example, if your error rate suddenly spikes above 1%, you can get an immediate notification.

---

## Profiling
Think of profiling as taking an X-ray of your application while it's running. It reveals:
- Which functions are taking the most time to execute
- Memory allocation and garbage collection patterns
- CPU usage across different threads
- Database query performance
- Hot spots in your code that need optimization

For example, profiling might reveal that a particular database query is taking 80% of your response time, helping you identify exactly what to optimize.

---

## Tracing

Imagine following a letter through the postal system - that's what tracing does for requests in your system:
- Follows a single request as it moves through different services
- Records timing at each step
- Shows the relationships between services
- Helps understand the full journey of a request

For example, when a user experiences slow checkout, tracing can show that it's because the payment service is slow, not the shopping cart service.

---
layout: image-right
image: https://plus.unsplash.com/premium_photo-1694740334454-36a9ad351a68?w=900&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8MXx8c3BlZWRvbWV0ZXJ8ZW58MHx8MHx8fDA%3D
---

These three tools work together to give you complete visibility:
- Counters tell you THAT something is wrong
- Profiling tells you WHY something is wrong within a service
- Tracing tells you WHERE something is wrong across services

When combined, these tools make troubleshooting much faster and more effective. Instead of guessing what might be wrong, you have concrete data pointing to the exact issue.

---
layout: section
---

## Log Ingestion

---
layout: section
---

### Built in integrations

---
layout: image
image: ./assets/Screenshot 2024-11-28 at 12.35.31 PM.png
backgroundSize: 80%
---

---
layout: section
---

### Custom Logs

---
layout: image
image: ./assets/Screenshot 2024-11-28 at 12.44.45 PM.png
backgroundSize: 80%
---



---

Suppose we have a web server that is producing logs like this:

```java
2024-02-05T09:47:36,919+06:00 INFO  com.ca.ekyc.activity.LogServiceImpl - Log Event - EventLog [id=0, entityId=-1, module=API_ACCESS, action=READ, message=Request to method: getUserCertificate, description=CertificateRequest [userId=01715297522], ipAddress=172.22.21.34, username=bcc-esign-api-user, datetime=2024-02-05T09:47:36.918970]
2024-02-05T09:47:47,040+06:00 INFO  com.ca.ekyc.user.service.AdssUserService - ADSS GetUser Found - UserId:  01715297522
2024-02-05T09:47:47,138+06:00 INFO  com.ca.ekyc.activity.LogServiceImpl - Log Event - EventLog [id=0, entityId=-1, module=CERTIFICATE, action=READ, message=ADSS  User certificate, description=ADSS user certificate using api call, ipAddress=172.22.21.34, username=bcc-esign-api-user, datetime=2024-02-05T09:47:47.137280]
2024-02-05T09:47:47,147+06:00 INFO  com.ca.ekyc.activity.LogServiceImpl - Log Event - EventLog [id=0, entityId=-1, module=API_ACCESS, action=READ, message=Response to method: getUserCertificate, description=ApiResponse [status=true, data=AdssCertificate [userId=01715297522, keyAlias=01715297522-311661bd-c1fe-4a78-b61a-6df9aaf158ca, keyStatus=ACTIVE], message=User certificate is found, statusCode=200, statusText=OK, path=/api/v1/user-certificate], ipAddress=172.22.21.34, username=bcc-esign-api-user, datetime=2024-02-05T09:47:47.147421]
2024-02-05T09:47:47,154+06:00 INFO  com.ca.ekyc.interceptor.CommonApiInterceptor - CommonApiInterceptor  Completed : Username: bcc-esign-api-user, Method: POST, Path: /api/v1/user-certificate, Status : 200
2024-02-05T09:47:47,457+06:00 INFO  com.ca.ekyc.api.AuthController - Login Request : Username = bcc-esign-api-user
2024-02-05T09:47:47,461+06:00 INFO  c.ca.ekyc.security.services.UserDetailsServiceImpl - Username: bcc-esign-api-user
2024-02-05T09:47:47,553+06:00 INFO  com.ca.ekyc.activity.LogServiceImpl - Log Event - EventLog [id=0, entityId=2, module=AUTH, action=READ, message=Login Request, description=Login is successful, ipAddress=172.22.21.34, username=bcc-esign-api-user, datetime=2024-02-05T09:47:47.457699]
2024-02-05T09:47:47,561+06:00 INFO  com.ca.ekyc.interceptor.CommonApiInterceptor - CommonApiInterceptor  Completed : Username: bcc-esign-api-user, Method: POST, Path: /api/auth/signin, Status : 200
2024-02-05T09:47:47,571+06:00 INFO  com.ca.ekyc.security.jwt.AuthTokenFilter - username: bcc-esign-api-user roles: [ROLE_CLIENT]
2024-02-05T15:08:35,622+06:00 ERROR com.ca.ekyc.api.RestSigningController - Get Certificate Error - UserId doesn't exist: 01517109340, Trace:
java.lang.Exception: UserId doesn't exist: 01517109340
        at com.ca.ekyc.user.service.AdssCertificateService.getUserCertificate(AdssCertificateService.java:188)
        at com.ca.ekyc.api.RestSigningController.getUserCertificate(RestSigningController.java:96)
        at com.ca.ekyc.api.RestSigningController$$FastClassBySpringCGLIB$$2ca0c3e.invoke(<generated>)
        at org.springframework.cglib.proxy.MethodProxy.invoke(MethodProxy.java:218)
        ...
        ...
```

---
layout: image-right
image: https://plus.unsplash.com/premium_photo-1673770408482-633babf2d18d?q=80&w=3087&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
---

### Ingest Pipeline

#### Multiline Configration

```yaml
multiline.pattern: '`^[0-9]{4}-[0-9]{2}-[0-9]{2}\s[0-9]{2}:[0-9]{2}:[0-9]{2}\.[0-9]{4}`'
multiline.negate: true
multiline.match: after
multiline.timeout: 15s
multiline.max_lines: 5000
```
---

#### Processor

```json
[
  {
    "grok": {
      "field": "message",
      "patterns": [
        "%{DATA:timestamp} \\[%{DATA:thread}\\] %{LOGLEVEL:level} %{JAVAFILE:class} - %{GREEDYMULTILINE:message}"
      ],
      "pattern_definitions": {
        "GREEDYMULTILINE": "(.|\n)*"
      }
    }
  }
]
```

#### Binding Processor to Custom Logs Integration

```yaml
pipeline: logs-signinghub-pipeline
```

---
layout: image
image: ./assets/spring.svg
backgroundSize: 50% 
---

## Network Schematic

---
layout: image
image: ./assets/Screenshot 2024-11-28 at 10.18.52 AM.png
backgroundSize: 80% 
---

## Logs in Elasticsearch Dashboard (Quicksign-API)

---
layout: iframe
url: https://kibana.bcc-ca.gov.bd:8888/app/r/s/agwth
---

---
layout: section
---

## Sample Dashboard (QuickSign-API)

---
layout: iframe
url: https://kibana.bcc-ca.gov.bd:8888/app/r/s/5bc3C
---

---
layout: section
---

## Sample Dashboard (BCC-CA-Boot)

---
layout: iframe
url: https://kibana.bcc-ca.gov.bd:8888/app/r/s/ZCGdI
showInToc: False
---


---
layout: section
---

## Synthetics

### Monitor

<img src="./assets/Screenshot 2024-12-01 at 11.00.40 AM.png" alt="Elastic Architecture" style="width: 80%; margin: 0 auto; padding:30px">


---
layout: iframe
url: https://kibana.bcc-ca.gov.bd:8888/app/synthetics
---

---
layout: section
---

## Sample APM Dashboard

---
layout: iframe
url: https://kibana.bcc-ca.gov.bd:8888/app/apm/services/bcc-ca-boot/overview?comparisonEnabled=true&environment=ENVIRONMENT_ALL&kuery=&latencyAggregationType=avg&offset=1d&rangeFrom=now-24h%2Fh&rangeTo=now&serviceGroup=&transactionType=request
---

---
layout: cover
---

## Alerts

---
layout: section
---

### Monitoring Alerts

---
layout: image
image: https://www.elastic.co/guide/en/kibana/current/images/alerting-overview.png
---

---
layout: image-right
image: https://cover.sli.dev
---

### Tools

- Built in Elastic Alerting / Kibana Alerts
- ElastAlert2
- Using the Elasticsearch API

---
layout: default
---

#### Built in Elastic Alerting / Kibana Alerts

<img src="./assets/Screenshot 2024-12-01 at 11.27.30 AM.png" alt="Elastic Architecture" style="width: 50%; margin: 0 auto; padding:30px">

---
layout: section
---

#### ElastAlert2

---
layout: iframe
url: https://elastalert2.readthedocs.io/en/latest/elastalert.html
---


---
layout: section
---

#### Using the Elasticsearch API

---
layout: image
image: ./assets/Screenshot 2024-12-01 at 11.39.06 AM.png
---

---
layout: cover
background: https://cover.sli.dev
---

## Real User Monitoring (RUM) / User Experience

---
layout: image
image: ./assets/user-experience-tab.png
backgroundSize: 80%
---

---
layout: center
class: text-center
---

---
layout: image
image: https://static-www.elastic.co/v3/assets/bltefdd0b53724fa2ce/blt617183d880a2a5fd/61849706a1ce11650a8d3528/screenshot-rum-across-hybrid-cloud.png

# Learn More

[Documentation](https://www.elastic.co/docs) · [Installation](https://www.elastic.co/guide/en/elasticsearch/reference/current/install-elasticsearch.html)

