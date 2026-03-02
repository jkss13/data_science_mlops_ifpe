# 📊 Data Science Project

## 🧾 Visão Geral

O **Data Science Project** é uma aplicação de Ciência de Dados voltada para a análise e visualização de dados históricos do mercado financeiro.

O projeto permite que usuários consultem o histórico de preços de ações de forma dinâmica por meio de um dashboard interativo. A coleta de dados é realizada via integração com o Yahoo Finance, enquanto a visualização é feita com gráficos interativos.

O objetivo principal é fornecer uma base organizada e reprodutível para análise exploratória de ativos financeiros, seguindo boas práticas de organização de projeto e gerenciamento de dependências.

---

## 🚀 Funcionalidades

### 🔎 Extração de Dados
- Integração com a API do Yahoo Finance utilizando a biblioteca `yfinance`
- Coleta de dados históricos de ações com base em:
  - Código do ativo
  - Intervalo de datas definido pelo usuário

### 📈 Visualização Interativa
- Geração de gráficos de séries temporais com `plotly`
- Destaque para o preço de fechamento (Close)
- Interface visual dinâmica e responsiva

### 🖥 Interface Web (Dashboard)
- Aplicação construída com `streamlit`
- Permite:
  - Inserir o código da ação
  - Definir o período de análise
  - Visualizar gráfico interativo
  - Visualizar tabela com dados brutos

### 📦 Gerenciamento de Dependências
- Utilização do `poetry`
- Ambiente virtual isolado
- Reprodutibilidade garantida

---

## 🏗 Estrutura do Projeto

O projeto está organizado de forma modular para facilitar manutenção e expansão.

### 📂 Módulos de Dados

#### `download_data`
Responsável por:
- Conectar à API do Yahoo Finance
- Baixar os dados históricos da ação selecionada

#### `get_current_date`
Responsável por:
- Garantir que a data final da consulta esteja sempre atualizada até o dia atual

---

### 📊 Módulo de Visualização

#### `plot_stock_data`
Responsável por:
- Receber os dados tratados
- Gerar gráfico interativo com Plotly
- Exibir o preço de fechamento ao longo do tempo

---

### 🧩 Aplicação Principal

A aplicação Streamlit integra todos os módulos e fornece uma interface onde o usuário pode:

- Digitar o código da ação (ex: PETR4.SA, AAPL, MSFT)
- Definir intervalo de datas
- Visualizar:
  - 📈 Gráfico interativo
  - 📋 Tabela com dados históricos

---

## ⚙️ Como Executar o Projeto

### 1️⃣ Instalar o Poetry

```bash
pipx install poetry
```

### 2️⃣ Instalar as dependências

```bash
poetry install
```

### 3️⃣ Ativar o ambiente virtual

```bash
source .venv/bin/activate
```

### 4️⃣ Executar a aplicação

```python
import mlopsdataproject as mdp
mdp.run_mlopsdataproject_app()
```

---

# 📊 2ª Etapa — Implementação de Indicadores Técnicos

> ⚠️ Esta etapa ainda não está implementada no repositório GitHub. Foi descrita com base nas aulas em que o projeto foi desenvolvido.

Após estruturar a base do projeto (coleta e visualização), o foco evoluiu para transformar dados brutos em **insights analíticos**, inspirando-se na plataforma TradingView.

---

## 🎯 Inspiração na TradingView

A proposta é permitir que o usuário não apenas visualize o preço da ação, mas também entenda sua tendência de mercado por meio de indicadores técnicos.

---

## 📉 Médias Móveis

As Médias Móveis foram escolhidas como primeiro indicador técnico.

### 📌 Objetivo
Suavizar flutuações de curto prazo e evidenciar a tendência principal do ativo.

### 📈 Tendência de Alta
Quando:
- O preço atual está acima da média móvel
- A média começa a se inclinar para cima

### 📉 Tendência de Baixa
Quando:
- O preço atual está abaixo da média móvel
- A média começa a se inclinar para baixo

---

## 💰 Lógica de Compra e Venda

Baseada no cruzamento entre o preço e a média móvel:

### 🟢 Sinal de Compra
- Quando o preço cruza a média móvel de baixo para cima
- Indica possível início de movimento de alta

### 🔴 Sinal de Venda
- Quando o preço cruza a média móvel de cima para baixo
- Indica possível início de movimento de baixa

---

## 📌 Objetivo do Projeto

O **Data Science Project** busca unir:

- Engenharia de dados
- Visualização interativa
- Organização modular
- Reprodutibilidade com MLOps
- Evolução para análise técnica automatizada

Servindo como base para projetos mais avançados de análise financeira.

````
