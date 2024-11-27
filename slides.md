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
layout: image-right
image: https://cover.sli.dev
hide: true
---

# Outline

- Observability
- Elastic Stack
  - Elasticsearch
  - Kibana
  - Elastic Agent
    - Beats
- Systems Performance Monitoring
- Application Monitoring
- Ingest Pipeline

---
layout: default
hideInToc: true
image: https://cover.sli.dev
---


# Presentation Outline

<Toc columns=2 />


---
layout: quote
background: https://cover.sli.dev
---

<style>

</style>

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
# Roles
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
layout: image
image: assets/Screenshot 2024-11-27 at 10.58.45 AM.png
backgroundSize: 80% 70%

---
## Inventory


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
layout: image
image: assets/Screenshot 2024-11-27 at 10.58.45 AM.png
backgroundSize: 80% 70%

---
## Inventory


---
layout: quote
---


# Applications Performance Monitoring

---
layout: default
---



# APM

- Tools
  - Counters
  - Profiling
  - Tracing

---
layout: center
class: text-center
---

---


---
layout: iframe
url: https://kibana.bcc-ca.gov.bd:8888/app/r/s/5bc3C
---
---


---
layout: center
class: text-center
---

# Learn More

[Documentation](https://sli.dev) · [GitHub](https://github.com/slidevjs/slidev) · [Showcases](https://sli.dev/resources/showcases)

<PoweredBySlidev mt-10 />
