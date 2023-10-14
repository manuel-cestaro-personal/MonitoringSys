# OpenVAS
Loki is a horizontally-scalable, highly-available, multi-tenant log aggregation system inspired by Prometheus. Loki differs from Prometheus by focusing on logs instead of metrics, and collecting logs via push, instead of pull.</br>
</br>
Loki is designed to be very cost effective and highly scalable. Unlike other logging systems, Loki does not index the contents of the logs, but only indexes metadata about your logs as a set of labels for each log stream.</br>
</br>
A log stream is a set of logs which share the same labels. Labels help Loki to find a log stream within your data store, so having a quality set of labels is key to efficient query execution.</br>
</br>
Log data is then compressed and stored in chunks in an object store such as Amazon Simple Storage Service (S3) or Google Cloud Storage (GCS), or even, for development or proof of concept, on the filesystem. A small index and highly compressed chunks simplify the operation and significantly lower the cost of Loki.</br>

## Start
EDIT
- `sudo mkdir /etc/prometheus`
- `sudo nano /etc/prometheus/prometheus.yml`
- copy and paste the file at `./config/prometheus.yml`
- create your docker network and replace `<yourNetwork>` in the `docker-compose` file
- run `docker-compose up -d`

## Grafana
After completing the login using `admin:admin` you need to add Loki to the datasource list using the following link: `http://loki:3100`</br>
Then import the following dashboards from the official Grafana repo:</br>
- https://grafana.com/grafana/dashboards/13639-logs-app/ (linux logs)
- https://grafana.com/grafana/dashboards/12611-logging-dashboard-via-loki/ (use V1, error in v2)


## Sources
- https://youtu.be/h_GGd7HfKQ8?si=nRbbutLCuoLvzOQf
- https://technotim.live/posts/grafana-loki/
- https://grafana.com/docs/loki/latest/
- https://grafana.com/oss/loki/
