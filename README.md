# 🚀 Ignition Zero: O Início da Aurora
## Missão Aurora Siger — Relatório Operacional de Pré-Decolagem

**Autor:** Francisco Wellington da Silva Rodrigues | **RM:** 566700  
**E-mail:** wellsimsousilva@gmail.com | **Instituição:** FIAP

---

## 📋 Sobre o Projeto

Relatório Operacional de Pré-Decolagem da nave **Aurora Siger**. 
O sistema lê dados de um arquivo CSV com **30 leituras de sensores** (intervalos de 5 min), analisa estatísticas históricas, detecta anomalias e emite o veredicto de decolagem.

**Tecnologias:** Python 3 · pandas · matplotlib · csv · ReportLab

---

## 📁 Estrutura do Repositório

```
ignition-zero-aurora/
├── aurora_missao.ipynb        # Notebook Jupyter principal
├── aurora_verificacao.py      # Script Python standalone
├── telemetria_aurora.csv      # Base de dados de telemetria (30 leituras)
└── README.md
```

---

## 📊 Base de Dados CSV

`telemetria_aurora.csv` — 30 leituras de sensores, 14 colunas:

| Coluna | Tipo | Descrição |
|---|---|---|
| timestamp | datetime | Data e hora da leitura |
| temperatura_interna | float | Temperatura interna da cabine (°C) |
| temperatura_externa | float | Temperatura ambiente externa (°C) |
| integridade_estrutural | int (0/1) | Integridade do casco |
| energia_banco_A/B/C | float | Carga de cada banco de baterias (%) |
| pressao_combustivel | float | Pressão do tanque de combustível (bar) |
| pressao_oxidante | float | Pressão do tanque de oxidante (bar) |
| modulo_* | int (0/1) | Status de cada módulo crítico |

---

## ⚙️ Requisitos

```bash
pip install pandas matplotlib jupyter
```

---

## ▶️ Como Executar

### Script Python (terminal)
```bash
python aurora_verificacao.py
```

### Jupyter Notebook
```bash
jupyter notebook aurora_missao.ipynb
```

---

## 📸 Print da Execução

```
==============================================================
   MISSAO AURORA SIGER - RELATORIO DE PRE-DECOLAGEM
   Fonte: telemetria_aurora.csv
==============================================================

[CSV] Base de dados carregada
  Total de leituras        : 30
  Periodo inicio           : 2025-01-15 06:00:00
  Snapshot para verificacao: 2025-01-15 08:25:00

[ESTATISTICAS] media | min -> max
  Temp. Interna (C)     :  25.80 |  21.40 ->  30.10
  Energia Banco A (%)   :  88.76 |  84.40 ->  93.00
  Pressao Comb. (bar)   : 317.23 | 308.20 -> 325.90

[VARREDURA HISTORICA] 30 leituras: OK - Sem anomalias.
[VERIFICACAO FINAL]   OK - Todos os parametros dentro das faixas.
--------------------------------------------------------------
RESULTADO: PRONTO PARA DECOLAR
--------------------------------------------------------------
```

---

## 📚 Referências

- NASA Autonomous Systems: https://www.nasa.gov
- ESA: https://www.esa.int
- SpaceX Starship: https://www.spacex.com/vehicles/starship

---
*FIAP — Ignition Zero 2025*
