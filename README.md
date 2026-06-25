# Processamento Analítico em Larga Escala para Extração Distribuída de Metafeatures

Este repositório contém a implementação desenvolvida para a disciplina de Ciência de Dados, cujo objetivo é investigar o uso do **Apache Spark** na construção de meta-bases para sistemas de **Meta-Aprendizagem** voltados à recomendação de técnicas de **Redução de Dimensionalidade (RD)**.

A proposta explora processamento distribuído, paralelismo e particionamento de dados para reduzir o custo computacional da extração de metafeatures em cenários envolvendo grandes volumes de dados.

---

## Objetivo

Desenvolver uma pipeline de processamento analítico em larga escala capaz de:

- Realizar a ingestão de conjuntos de dados provenientes do OpenML;
- Executar a extração distribuída de metafeatures utilizando Apache Spark;
- Construir uma meta-base para sistemas de meta-aprendizagem;
- Avaliar técnicas de redução de dimensionalidade;
- Treinar um meta-modelo para recomendação automática de técnicas de RD.

---

## Arquitetura

A pipeline proposta é composta pelas seguintes etapas:

1. Ingestão dos datasets (OpenML)
2. Filtragem dos conjuntos de dados
3. Conversão para formato Parquet
4. Particionamento utilizando Apache Spark
5. Extração distribuída de metafeatures
6. Avaliação das técnicas de Redução de Dimensionalidade
7. Construção da meta-base
8. Treinamento do meta-modelo
9. Recomendação de técnicas de RD

---

## Tecnologias Utilizadas

- Apache Spark
- Python
- PySpark
- OpenML
- PyMFE
- Scikit-Learn
- Pandas
- NumPy

---

## Metafeatures

A extração foi realizada utilizando a biblioteca **PyMFE**, considerando os seguintes grupos de metafeatures:

- Landmarking
- General
- Statistical
- Model-based
- Information Theory
- Relative
- Clustering
- Complexity
- Itemset
- Concept

Também foram utilizados operadores de sumarização estatística:

- Mean
- Median
- Minimum
- Maximum
- Standard Deviation
- Quantiles
- Histogram

---

## Técnicas de Redução de Dimensionalidade

Foram avaliadas as seguintes técnicas:

- PCA
- Incremental PCA
- Random Trees Embedding
- SelectKBest
- Spectral Embedding
- Truncated SVD
- Linear Discriminant Analysis (LDA)
- Locally Linear Embedding (LLE)
- Kernel PCA
- t-SNE

---

## Meta-Aprendizagem

O sistema utiliza um **Random Forest Regressor** como meta-modelo para aprender a relação entre as metafeatures dos conjuntos de dados e o desempenho das técnicas de redução de dimensionalidade.

A avaliação foi realizada utilizando:

- Leave-One-Out Cross Validation (LOOCV)
- Spearman Rank Correlation (SRC)

Os resultados foram comparados com os seguintes métodos de referência:

- Mean Ranking
- Median Ranking

---

## Estrutura do Projeto

```text
.
├── data/
│   ├── raw/
│   ├── parquet/
│   ├── metafeatures/
│   └── rankings/
│
├── notebooks/
│
├── src/
│
├── figures/
│
├── report/
│
└── README.md
```

---

## Resultados

A utilização do Apache Spark permitiu distribuir a etapa de extração de metafeatures entre múltiplas partições, reduzindo o custo computacional da construção da meta-base e tornando a solução escalável para cenários envolvendo centenas de conjuntos de dados.

O meta-modelo apresentou desempenho superior aos métodos de referência (Mean Ranking e Median Ranking), demonstrando a capacidade de aprender relações entre as metafeatures e o desempenho das técnicas de redução de dimensionalidade.

---

## Autor

**Daniel José da Silva**

Mestrando em Informática

Universidade Federal de Alagoas (UFAL)
