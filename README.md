
#  Previsão de Score de Crédito com Inteligência Artificial

## Visão Geral do Projeto
Este projeto foi desenvolvido durante a Jornada Python da Hashtag Treinamentos como parte de um estudo prático de **Inteligência Artificial e Machine Learning**. O objetivo é auxiliar uma instituição financeira na análise e classificação automática do **Score de Crédito** dos seus clientes nas categorias: **Ruim**, **Ok** ou **Bom**.

A solução utiliza algoritmos de Machine Learning capazes de processar o histórico e perfil dos clientes para prever a classificação de novos utilizadores com alta precisão.

---

## Tecnologias e Bibliotecas Utilizadas
* **Python** (Linguagem principal)
* **Pandas**: Manipulação, limpeza e análise de dados estruturados.
* **Scikit-Learn (`sklearn`)**: 
  * `LabelEncoder`: Pré-processamento e conversão de variáveis categóricas (texto) em formato numérico.
  * `train_test_split`: Divisão da base de dados em conjuntos de treino (70%) e teste (30%).
  * `RandomForestClassifier`: Algoritmo baseado em Árvores de Decisão.
  * `KNeighborsClassifier` (KNN): Algoritmo de classificação baseado em vizinhos mais próximos.
  * `accuracy_score`: Avaliação do desempenho e precisão dos modelos.

---

## Passo a Passo da Solução

1. **Carregamento dos Dados:** Leitura e preparação do histórico de clientes utilizando a biblioteca Pandas.
2. **Pré-processamento (Encoding):** Tratamento de colunas de texto (`profissao`, `mix_credito`, `comportamento_pagamento`) convertendo-as em números com o `LabelEncoder`.
3. **Divisão de Variáveis e Dados:** 
   * Separação das variáveis explicativas ($X$) e do alvo/target ($y = \text{score\_credito}$).
   * Divisão em dados de treino e teste.
4. **Treino dos Modelos:** Treinamento paralelo de dois modelos de Machine Learning (**Random Forest** e **KNN**).
5. **Avaliação do Desempenho:** Comparação da acurácia de cada modelo para escolha da melhor opção de produção.
6. **Previsão em Novos Clientes:** Aplicação do modelo treinado (`RandomForestClassifier`) sobre uma nova base de clientes (`novos_clientes.csv`) para classificação automática do score.

---