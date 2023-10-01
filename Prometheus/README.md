# OpenVAS
Prometheus is an open-source systems monitoring and alerting toolkit originally built at SoundCloud. Since its inception in 2012, many companies and organizations have adopted Prometheus, and the project has a very active developer and user community. It is now a standalone open source project and maintained independently of any company.</br>
To emphasize this, and to clarify the project's governance structure, Prometheus joined the Cloud Native Computing Foundation in 2016 as the second hosted project, after Kubernetes.</br>
</br>
Prometheus collects and stores its metrics as time series data, i.e. metrics information is stored with the timestamp at which it was recorded, alongside optional key-value pairs called labels.</br>

## Start
- `sudo mkdir /etc/prometheus`
- `sudo nano /etc/prometheus/prometheus.yml`
- copy and paste the file at `./config/prometheus.yml`
- create your docker network and replace `<yourNetwork>` in the `docker-compose` file
- run `docker-compose up -d`

## Grafana
After completing the login using admin:admin you need to add Prometheus to the datasource list using the following link: `http://prometheus:9090`</br>
Then import the following dashboards from the official Grafana repo:</br>
- https://grafana.com/grafana/dashboards/1860-node-exporter-full/
- https://grafana.com/grafana/dashboards/14282-cadvisor-exporter/


## Sources
- https://youtu.be/9TJx7QTrTyo?si=O4GzKUg6b0Cj_uRX
- https://github.com/ChristianLempa/boilerplates
- https://prometheus.io/