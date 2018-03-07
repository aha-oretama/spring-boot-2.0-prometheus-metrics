# spring-boot-2.0-prometheus-metrics

This is the sample repository for monitoring Spring Boot 2.0 by [Prometheus](https://prometheus.io/). 

Spring Boot 2.0 include [Micrometer](https://micrometer.io/docs), which provides a simple facade over the instrumentation clients for the most popular monitoring systems.

See [pom.xml](https://github.com/aha-oretama/spring-boot-2.0-prometheus-metrics/blob/master/pom.xml)!  
That only setting makes your application monitored!!

## How to run

Substitute `your_ip` in prometheus.yml and `path_prometheus_yml` in the following command.

After you execute the following command,
Spring Boot application and Prometheus will start up on `8080` and `9090` port respectively. 

```bash
$ ./mvnw spring-boot:run
```

```bash
$ docker run -p 9090:9090 -v path_prometheus_yml:/etc/prometheus/prometheus.yml prom/prometheus
```

## Access

| Application | Url |
| ---------- | ------- |
| Spring Boot | http://localhost:8080/actuator/prometheus |
| Prometheus | http://localhost:9090/graph |
