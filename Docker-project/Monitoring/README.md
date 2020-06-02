Monitoring and Alerting with Docker

Logging Stack: Loki, Promtail and Grafana

Web Interface: Traefik

Requirement before running compose file


Hardening OS


Install docker


Install docker-compose


Change and complate config files



Installation
Step1: chnage service config files:

tree logging
.
|-- README.md
|-- docker-compose.yml
|-- loki
|   `-- local-config.yaml
`-- promtail
    `-- docker-config.yaml

2 directories, 4 files
Step2: chnage DOMAIN on docker-comose file with your domain.

Step3: change promtail config

Step4: check compose file and Run all services
docker-compose config
docker-compose up -d

Step5: Check compose services and view all services logs
docker-compose ps
docker-compose logs -f --tail 100

Step6: check and visit your domain service:


loki.DOMAIN: loki web interface


web.DOMAIN: traefik2 dashboard


grafana.DOMAIN: grafana dashboard


Step7: config grafana service for view all log on Explore menu
