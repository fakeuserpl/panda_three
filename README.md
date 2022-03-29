# Panda three

## Build

Instruction how to build project using gradle is here: 
https://spring.io/guides/gs/gradle/


    
## Prometheus

Prometheus is a free event monitoring and alerting software application. It logs real-time metrics in a time series database built with an HTTP pull model, allowing for flexible queries and real-time alerting. <br/>
To run it locally, download Prometheus, and change prometheus.yml file. <br/> In the section scrape-config add:

```
- job_name: 'panda-three-app'
    metrics_path: '/prometheus'
    scrape_interval: 5s
    static_configs:
      - targets: ['localhost:8091']
