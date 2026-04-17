# Docker Compose Stacks

Production-ready Docker Compose stacks for the most common services. Each stack is self-contained, documented, and ready to run.

## Available Stacks

| Stack | Services | Description |
|-------|----------|-------------|
| `lemp/` | Nginx, PHP-FPM, MariaDB | Classic web server stack |
| `monitoring/` | Prometheus, Grafana, cAdvisor, Node Exporter | Full observability |
| `elk/` | Elasticsearch, Logstash, Kibana | Centralized logging |
| `redis-sentinel/` | Redis + 2 Sentinels | HA Redis setup |
| `wordpress/` | WordPress, MariaDB, Redis, Nginx | Production WordPress |

## Quick Start

```bash
# Clone the repo
git clone https://github.com/alibadra/docker-compose-stacks.git
cd docker-compose-stacks

# Copy and edit the env file
cp .env.example .env
nano .env

# Start a stack
cd lemp
docker compose up -d
```

## Requirements

- Docker >= 24.0
- Docker Compose >= 2.20

## Structure

```
.
├── lemp/
│   ├── docker-compose.yml
│   ├── nginx/default.conf
│   └── php/php.ini
├── monitoring/
│   ├── docker-compose.yml
│   ├── prometheus/prometheus.yml
│   └── grafana/provisioning/
├── elk/
│   ├── docker-compose.yml
│   └── logstash/pipeline/
├── redis-sentinel/
│   └── docker-compose.yml
└── wordpress/
    └── docker-compose.yml
```

## Contributing

PRs are welcome. Please keep each stack minimal and focused.
