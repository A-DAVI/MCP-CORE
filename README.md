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

## Estrutura de Pastas (BLOQUEADA)

Esta estrutura é **oficial e imutável**.  
Alterações fora das regras descritas aqui **quebram o projeto conceitualmente**.

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
Regras de Bloqueio Estrutural
Estrutura Imutável
Os itens abaixo não podem ser renomeados, removidos ou ter sua função alterada:

server.py

core/

rules/

contracts/

templates/

Estrutura Extensível
Os itens abaixo podem crescer, respeitando o padrão existente:

tools/
Novas ferramentas podem ser adicionadas, as existentes não devem ser removidas.

agents/
Cada agent deve ser uma pasta própria contendo:

prompt.md

agent.py

constraints.yaml

tests/
Testes devem acompanhar qualquer evolução do projeto.

Regras Fundamentais de RPA (v1)
Regras Obrigatórias
Todo RPA deve possuir:

logging estruturado

configuração externa

tratamento global de exceções

Credenciais:

É proibido hardcode

Devem vir de vault ou secret manager

Falhas:

Devem ser previsíveis

Devem gerar log contextual

Regras de Qualidade
Proibido uso de sleep sem justificativa

Funções devem ser idempotentes sempre que possível

Entrada e saída devem ser claramente definidas

Agents — Versão Inicial
Agent: RPA Architect
Responsabilidades

Avaliar o tipo de automação

Sugerir arquitetura adequada

Ajustar templates ao contexto

Exemplos de decisões

Batch vs event-driven

Necessidade de retry

Impacto de volume, frequência e criticidade

Limitações

Não gera código final

Não altera regras

Apenas recomenda

Fluxo de Execução
Usuário faz a solicitação

MCP recebe o pedido

MCP decide quais agents consultar

Agents analisam e retornam recomendações

MCP valida regras obrigatórias

MCP executa a ação final

MCP entrega resultado auditável

Princípios do Projeto
Regras explícitas são melhores que decisões implícitas

Simplicidade antes de generalização

Determinístico antes de inteligente

Documentação faz parte do código

MCP serve o desenvolvedor, não o contrário

Evolução Futura (Planejada)
Agent de Segurança

Agent de Code Review

Integração com robótica / automação física

Métricas de conformidade

Histórico de decisões técnicas      
