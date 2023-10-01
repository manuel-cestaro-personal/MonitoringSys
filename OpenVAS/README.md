# OpenVAS
OpenVAS is a full-featured vulnerability scanner. Its capabilities include unauthenticated and authenticated testing, various high-level and low-level internet and industrial protocols, performance tuning for large-scale scans and a powerful internal programming language to implement any type of vulnerability test.</br>
The scanner obtains the tests for detecting vulnerabilities from a feed that has a long history and daily updates.</br>
</br>
OpenVAS has been developed and driven forward by the company Greenbone since 2006. As part of the commercial vulnerability management product family Greenbone Enterprise Appliance, the scanner forms the Greenbone Community Edition together with other open-source modules.</br>

## Start
- create your docker network and replace `<yourNetwork>` in the `docker-compose` file
- run `docker-compose up -d`
- check the startup process with `docker logs -f openvas` (it could take up to 1 hour)
</br></br>
In order to update CVE and NVT restart the container periodically.


## Sources
- https://github.com/immauss/openvas
- https://hub.docker.com/r/immauss/openvas
- https://immauss.github.io/openvas/
- https://docs.greenbone.net/GSM-Manual/gos-22.04/en/
