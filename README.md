# Observabilidade

Este repositório contém as ferramentas necessárias para a observabilidade do sistema. É importante ressaltar que seu uso é destinado exclusivamente para testes. Caso deseje utilizá-lo em produção, recomendo consultar a documentação de cada ferramenta para seguir as práticas mais seguras.

As seguintes ferramentas serão instaladas.

- Elasticsearch
- Kibana
- Grafana
- Prometheus
- Jaeger
- Node exporter
- Otel Opentelemetry Collector

## Elasticsearch
Descrição: É utilizado para armazenar dados indexados, oferecendo maior performance e rapidez nas consultas. Qualquer tipo de dado pode ser armazenado, pois utiliza o conceito de JSON.

Porta: ```9200``` 

Exemplo: https://localhost:9200

Use para se conectar com o elasticsearch, necessário inserir o usuário e senha ou configurar um API KEY.

## Kibana
Descrição: Utilizado para integrar a parte visual ao Elasticsearch, permitindo a configuração de dashboards para visualizações e diversas outras funcionalidades.

Porta: ```5601``` 

Exemplo: http://localhost:5601

Use para acessar o front do kibana, caso necessário tente usar a guia anônima do navegador.

## Grafana
Descrição: Utilizado para exibir dashboards relacionados ao Prometheus e ao Node Exporter.

Porta: ```3000``` 

Exemplo: http://localhost:3000

Use para acessar o front do grafana.

## Prometheus
Descrição: Utilizado para realizar o scraping dos arquivos de métricas do Node Exporter.

Porta: ```9090``` 

Exemplo: http://localhost:9090

Use para acessar o front do prometheus.

## Jaeger
Descrição: Utilizado para rastreamento de traces. É necessário que o projeto esteja instrumentado com OpenTelemetry para que os traces possam ser recebidos.

Porta: ```16686``` 

Exemplo: http://localhost:16686

Use para acessar o front do jaeger.

## Node exporter:
Descrição: Utilizado para coletar métricas da máquina.

## Otel Collector:
Descrição: Apenas o coletor está configurado no docker compose é necessário instalar o OpenTelemetry no projeto para completar a integração.

Porta: ```14300``` 

Usada para coletar métricas, traces e logs, mas a implementação depende de como você a configura no seu projeto.
ex: ```127.0.0.1:14300```

[Link da documentação para configurar o opentelemetry no projeto](https://opentelemetry.io/docs/languages/php/getting-started/)
