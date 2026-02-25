
# Observability Pack (Fixed)

- Grafana exposto em 3003
- cAdvisor e Node Exporter sem portas públicas (scrape interno via Prometheus)
- Alloy montado via pasta (`./alloy:/etc/alloy:ro`) com config.alloy presente

## Deploy
- Coolify → Git Source (ou Service → Docker Compose)
- Ajuste domínios apenas para Grafana (3003) e, opcionalmente, Prometheus (9090)

## Acesso
- Grafana: http://HOST:3003 (admin/admin)
- Prometheus: http://HOST:9090
