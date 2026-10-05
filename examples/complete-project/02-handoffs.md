# 02 — Handoffs

## Arquitetura → Conteúdo

```text
OUTPUT: formato do documento e estados draft/published
CONTRACT: busca só recebe published
VERIFY: exemplos obedecem ao schema
STATUS: PASS
RISK: versionamento ainda não foi implementado
```

## Arquitetura → Busca

```text
OUTPUT: interface de consulta por título, categoria e texto
CONTRACT: resultados incluem id, título, categoria e status
VERIFY: casos vazios e correspondência parcial definidos
STATUS: PASS CONTROLADO
RISK: desempenho em grandes volumes não verificado
```

## Busca → Interface

```text
OUTPUT: formato estável de resultado
CONTRACT: interface não exibe documentos draft
VERIFY: fluxo de resultado, vazio e erro descrito
STATUS: PASS CONTROLADO
RISK: acessibilidade completa ainda não verificada
```
