
# Observability Pack (Loki + Alloy + Grafana + Prometheus + Node Exporter + cAdvisor)

## Como usar no Coolify
1. Crie um **Service → Docker Compose** em um novo projeto (ex.: `observability`).
2. Faça upload do conteúdo deste pacote e aponte para o `docker-compose.yml`.
3. Crie volumes persistentes (Coolify cria automaticamente para os volumes nomeados deste compose).
4. Faça deploy. Acesse:
   - Grafana: `http://<host>:3000` (admin/admin)
   - Loki API: `http://<host>:3100`
   - Prometheus: `http://<host>:9090`
   - Alloy UI: `http://<host>:12345`

## Datasources/Alerts
- Datasources do Grafana são provisionados automaticamente (Prometheus e Loki).
- Um dashboard inicial e três alertas (CPU, Memória, Reinício de containers) já vêm prontos.

## Notas
- Ajuste as senhas e crie **Contact Points** no Grafana para receber alertas (Email/Telegram/Slack/etc.).
- Para reduzir cardinalidade em Loki, adicione labels apenas necessárias; evite IDs únicos como label.
- Pin versions em produção (atualize as tags das imagens no `docker-compose.yml`).
