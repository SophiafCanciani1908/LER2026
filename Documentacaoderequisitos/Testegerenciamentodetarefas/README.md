# Sistemas de Gestão de Tarefas - Especificação de Requisitos 

### 1. Introdução

### 1.1 Propósito 

Este documento especifíca os requisitos funcionais e não-funcionais para os Sistemas de Gestão de Tarefas (SGT) Seguindo o Padrão IEEE 29148.

### 1.2 Escopo 

O SGR permitirá que úsuarios criem, organizem e acompanhem tarefas pessoais e profissionais com sistema de prioridades e prazos.

### 1.3 Definição e Acrônimos

- **SGT**: Sistemas de Gestão de Tarefas
- **RF**: Requisitos Funcionais
- **RNF**: Requisitos Não-Funcionais
- **Sprint**: Período de 2 semanas de Desenvolvimento
  
## 2. Descrição Geral

### 2.1 Pespectiva do Produto 

O SGT será uma aplicação web responsiva com sincronização em nuvem

### 2.2 Funções Principais

- Criação e edição de tarefas
- Organização por projetos e tags 
- Sistema de notificação
- Relatório de produtividade

## 3. Requisitos Específicos 

### 3.1 Requisitos Funcionais

#### RF-001: Criação de Tarefas

**Descrição**: O Sistema deve permitir que o úsuario criem tarefas com título, descrição, data de vencimento e prioridade.
**Prioridade**: Alta
**Versão**: 1.0
**Data**: 2026-03-25
**Rastreabilidade**: Derivado de Necessidade do StakeHolder NS-001
**Critérios de Aceitação**: 

- [ ] Usuário pode criar, editar e excluir tarefa
- [ ] Formulário com campos obrigatórios (título) e opcionais
- [ ] Níveis de prioridade: Baixa, Média, Alta, Urgente
- [ ] Confirmação Visual após Criação 
- [ ] Validação de dados da tarefas (não permitir datas vazias)
  
---

### RF-002: Organização por Projetos

**Descrição**: O sistema deve permitir agrupar tarefas em projetos personalizados
**Prioridade**: Média
**Versão**: 1.0
**Data**: 2026-03-25
**Rastreabilidade**: Derivado de NS-002
**Critérios de Aceitação**: 

- [ ] Usuário pode criar, renomear e excluir projetos
- [ ] Tarefas podem ser atribuídas a um ou mais projetos
- [ ] Visualização filtrada por projetos
  
---

### 3.2 Requisitos Não-Funcionais

#### RNF-001: Desempenho

**Descrição**: O sistema deve carregar a lista de tarefas em menos de 1 segundo para até 100 tarefas.
**Categorias**: Desempenho 
**Prioridade**: Alta
**Versão**: 1.0
**Métrica**: Tempo de resposta < 1s para 95% das resquisiçãoes

---

#### RNF-002; Segurança

**Descrição**: O sistema deve implementar autentificação Oauth 2.0 e criptografia TLS 1.3
**Categoria**: Segurança
**Prioridade**: Crírica
**Versão**: 1.0
**Métrica**: Conformidade LGPD, DPR

---

## 4. Controle de Versões

### Histórico de Alterações

|Versão|Data|Autor|Modificação|
|------|----|-----|-----------|
| 1.0  |2026-03-25|SophiaCanciani|Versão Inicial|

### Ratreabilidade

Gráfico de Rastreabilidade

```mermaid

graph TD

    NS001['NS-001: Necessidade StakeHolder] --> RF001['RF-001: Criação Tarefas']
    RF001 --> TC001['TC-001: Criação'] 

    NS002['NS-002: Organização']--> RF002['RF-002: Projetos']
    RF002 --> TC002 ['TC-002: Teste Projetos']

```
