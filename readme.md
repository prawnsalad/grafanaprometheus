## Local metrics

Run Grafana and Prometheus locally in docker containers, ~100mb memory usage.

Get going as quickly as possible, just run:
> start.sh

- Grafana: http://localhost:3000/
  No login required by default.
- Prometheus: http://localhost:9090/
  You probably don't want this. Dashboards and graphs are done via grafana.

#### Structure
- `grafana/` - Grafana configuration. Simplistic and barebones
- `grafana_data/` - Grafana runtime data. Stores your dashboards and user settings. Created when Grafana first runs.
- `prometheus/` - Prometheus configuration. Includes scraping config files. Each `prometheus/*.scrape.yml` file is loaded allowing you to add custom promethris scraping URLs as needed without checking them into git.
- `prometheus_data/` - Prometheus runtime data. Stores all the metrics database. Created when Prometheus first runs. Don't modify this stuff.

#### Scripts
- `start.sh` - Start prometheus and grafana containers.
