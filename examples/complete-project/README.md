# Exemplo completo: Knowledge Hub

Este exemplo simula a evolução de um pequeno portal de conhecimento com busca, categorias e revisão editorial. O objetivo é demonstrar o método, não fornecer um produto pronto para produção.

## Objetivo

Criar uma base de conhecimento navegável com conteúdo organizado, busca por texto e fluxo simples de revisão.

## Não objetivos

- autenticação real;
- publicação em produção;
- integração com banco de dados;
- garantia de desempenho em escala.

## Arquitetura inicial

```text
conteúdo -> catálogo -> busca -> interface
              |          |
              +-> revisão +-> evidências
```

Contratos principais:

- o catálogo define o formato dos documentos;
- a busca consome apenas documentos publicados;
- a interface não decide regras editoriais;
- o revisor de evidências não altera a implementação.

## Agentes e frentes

| Frente | Agente | Saída | Dependência |
|---|---|---|---|
| Arquitetura | architecture-coordinator | mapa, contratos e divisão | briefing |
| Conteúdo | content-builder | documentos de exemplo | contrato do catálogo |
| Busca | search-builder | estratégia e casos de busca | catálogo |
| Interface | experience-builder | fluxo de navegação | catálogo e busca |
| Validação | evidence-reviewer | registro de evidências | todas as frentes |

## Regra de handoff

Cada frente entrega:

1. arquivos ou decisões produzidos;
2. contratos respeitados;
3. verificação executada;
4. riscos e pontos não verificados;
5. impacto para as outras frentes.

## Resultado simulado

- arquitetura: `PASS`;
- catálogo e conteúdo de exemplo: `PASS CONTROLADO`;
- busca: `PASS CONTROLADO` — casos locais cobertos, desempenho não medido;
- interface: `PASS CONTROLADO` — fluxo revisado, acessibilidade completa não verificada;
- publicação real: `NOT_VERIFIED`.

O projeto pode avançar para uma demonstração local, mas ainda não pode ser declarado pronto para produção.
