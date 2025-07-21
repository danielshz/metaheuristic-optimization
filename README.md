# Comparativo de Algoritmos Evolutivos em Funções Benchmark

Este repositório contém implementações e experimentos de quatro algoritmos de otimização por meta-heurísticas:

- Algoritmo Genético (AG)
- Evolução Diferencial (DE)
- Otimização por Enxame de Partículas (PSO)
- C-DEEPSO (Canonical DEEPSO)

As comparações foram feitas com base em funções de benchmark conhecidas em diferentes dimensões.

## 📓 Notebook

O notebook [`trabalho_final.ipynb`](./trabalho_final.ipynb) contém **todo o fluxo reprodutível**, incluindo:

- Implementação dos algoritmos
- Definição das funções de benchmark
- Ajuste de hiperparâmetros com Optuna
- Execução dos experimentos
- Análises estatísticas (Friedman, Nemenyi)
- Geração de gráficos: boxplots, curvas de convergência, heatmaps

## 📌 Objetivo

Avaliar o desempenho relativo dos algoritmos em termos de:
- Qualidade da solução
- Velocidade de convergência
- Robustez e estabilidade
- Diferença estatística significativa

## ⚙️ Metodologia

- Funções benchmark: **Rosenbrock** (unimodal) e **Rastrigin** (multimodal)
- Dimensões testadas: 10, 30, 50
- 30 execuções independentes por cenário
- População de 100 indivíduos
- Parâmetros otimizados com [Optuna](https://optuna.org/)
- Avaliação com testes estatísticos: Friedman e Nemenyi

## 📊 Principais Resultados

- **DE** teve o melhor desempenho médio geral.
- **C-DEEPSO** apresentou melhor estabilidade e desempenho em alta dimensão.
- **PSO** foi competitivo apenas em baixa dimensão.
- **AG** teve o pior desempenho em cenários multimodais.

## 📂 Estrutura

```
.
├── trabalho_final.ipynb       # Notebook completo e reprodutível
├── trabalho_final.pdf         # Artigo em PDF com descrição dos métodos e resultados
└── README.md
```

## 🧰 Requisitos

- Python 3.8+
- numpy, scipy, matplotlib, seaborn
- pandas, optuna, scikit-learn

## 📜 Referências

- [Virtual Library of Simulation Experiments](https://www.sfu.ca/~ssurjano/optimization.html)
- Artigos sobre algoritmos evolutivos, Optuna, e testes estatísticos (ver PDF)

**Autor**: Daniel Arruda Ponte  
**Data**: Julho de 2025
