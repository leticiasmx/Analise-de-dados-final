# Análise de Salários no Mercado de Dados Brasileiro — 2024

**Sammya & Petrick | 5º Período — Engenharia de Software | UNIFSA**  
Disciplina: Análise Avançada de Dados | Profa. Ma. Heloisa Guimarães

---

## Dashboard

🔗 [Acessar o dashboard no Google Looker Studio](https://datastudio.google.com/reporting/62f950b4-c618-4c1e-aa82-bb08b3a86ef4)

---

## Pergunta central

> Quais fatores mais influenciam o salário de um profissional de dados no Brasil em 2024?

O nível de cargo e o tempo de experiência em dados são os dois fatores com maior influência sobre o salário — com correlações de Spearman de **r = 0,73** e **r = 0,66**, respectivamente. Um Júnior com menos de 1 ano de experiência recebe mediana de R$3.500. Um Sênior com mais de 10 anos chega a R$22.500 — **6,4 vezes mais**.

O achado mais relevante é que tempo de experiência sozinho não garante progressão salarial. O maior salto acontece na transição formal de Pleno para Sênior. Um profissional com 7 anos de experiência, mas sem mudança de nível, pode ganhar menos do que um Sênior com 3 anos. O mercado reconhece o cargo que você ocupa, não só o tempo que você acumulou.

Outros fatores identificados: região (Sudeste, especialmente SP, tem medianas maiores), gênero (homens ganham em mediana ~R$2.000 a mais, diferença que persiste mesmo controlando pela senioridade) e formação acadêmica (pós-graduação correlaciona com salários maiores, mas com efeito menor do que o nível de cargo).

---

## Principais decisões de limpeza

| Problema | Decisão tomada |
|---|---|
| Salário em faixas de texto | Convertido para ponto médio numérico (ex: "de R$4.001 a R$6.000" → R$5.000) |
| Colunas com nomes crípticos (P1_a, P2_b_1...) | Renomeadas usando o dicionário oficial do Kaggle |
| Cargos com títulos inconsistentes | Agrupados em categorias padronizadas com critérios documentados no notebook |
| Ausências em gênero e raça/cor | Não imputadas — ausência de resposta é uma escolha, não um erro |
| Ferramentas codificadas em 0/1 | Tratadas como variáveis binárias independentes |

---

## Estrutura do repositório

```
sammya-petrick-state-of-data/
├── README.md
├── notebook/
│   └── sammya-petrick-analise.ipynb
├── relatorio/
│   └── sammya-petrick-relatorio.pdf
└── dados/
    └── README.md
```

---

## Como reproduzir a análise

1. Baixe a base em: [kaggle.com/datasets/datahackers/state-of-data-brazil-20242025](https://www.kaggle.com/datasets/datahackers/state-of-data-brazil-20242025)
2. Abra o notebook no Google Colab
3. Faça upload do CSV quando solicitado na primeira célula
4. Execute todas as células em ordem

**Dependências:** pandas, numpy, matplotlib, seaborn, scipy

---

## Referências

- DATA HACKERS; BAIN & COMPANY. *State of Data Brazil 2024–2025*. Disponível em: kaggle.com/datasets/datahackers/state-of-data-brazil-20242025
