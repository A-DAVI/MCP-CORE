# MCP RPA — Padronização de Desenvolvimento com Agents

## Visão Geral

Este projeto define um **MCP (Model Context Protocol)** voltado para **padronização, aceleração e validação do desenvolvimento de RPAs** no escritório.

O MCP **não é um chatbot** e **não é um assistente genérico**.  
Ele funciona como **infraestrutura técnica**, impondo padrões, controlando decisões e reduzindo erros recorrentes no desenvolvimento de automações.

> Princípio central do projeto:  
> **Agents aconselham. MCP decide.**

---

## Objetivo do Projeto

- Padronizar o desenvolvimento de RPAs
- Reduzir retrabalho e inconsistências técnicas
- Acelerar a criação de novos projetos
- Servir como memória técnica e guardião de padrões
- Permitir crescimento futuro sem caos arquitetural

O MCP deve:
- Gerar RPAs padronizados
- Validar RPAs existentes
- Explicar regras e decisões técnicas
- Escalar com agents especializados, sem perder controle

---

## Escopo Inicial (MVP)

O MCP v1 cobre **três responsabilidades principais**:

### 1. Criação de RPA
- Geração de estrutura base
- Aplicação automática de padrões
- Inclusão obrigatória de:
  - logging estruturado
  - configuração externa
  - tratamento global de erros
  - retry e timeout padrão

---

### 2. Validação de RPA
- Análise de projetos existentes
- Identificação de desvios de padrão
- Classificação de riscos:
  - Crítico
  - Alerta
  - Informativo

---

### 3. Explicação de Padrões
- Justificativa técnica das regras
- Quando uma regra pode ser quebrada
- Impacto técnico de ignorar o padrão

---

## Arquitetura Conceitual

### MCP Core
Responsável por:
- Expor ferramentas
- Controlar o fluxo de execução
- Aplicar regras obrigatórias
- Consolidar respostas dos agents
- Tomar a decisão final

---

### Agents
Responsáveis por:
- Análise contextual
- Recomendações técnicas
- Avaliação especializada

Os agents **não**:
- Criam padrões
- Quebram regras
- Executam ações finais
- Alteram estrutura do projeto

---
## Estrutura do Projeto

```text
mcp-rpa/
├── README.md
├── pyproject.toml
├── server.py
│
├── core/
│   ├── __init__.py
│   ├── context.py
│   ├── router.py
│   ├── executor.py
│   └── exceptions.py
│
├── rules/
│   ├── rpa_rules.yaml
│   └── README.md
│
├── tools/
│   ├── __init__.py
│   ├── create_rpa.py
│   ├── validate_rpa.py
│   └── explain_rules.py
│
├── agents/
│   ├── __init__.py
│   └── rpa_architect/
│       ├── __init__.py
│       ├── prompt.md
│       ├── agent.py
│       └── constraints.yaml
│
├── templates/
│   └── python_rpa/
│       ├── main.py.jinja
│       ├── config.yaml.jinja
│       └── README.md
│
├── contracts/
│   ├── tool_contracts.yaml
│   └── agent_contracts.yaml
│
├── logs/
│   └── .gitkeep
│
├── tests/
│   ├── test_rules.py
│   ├── test_tools.py
│   └── test_agents.py
│
└── .gitignore
text´´´´

Métricas de conformidade

Histórico de decisões técnicas      
