# Star Classification Model

Este projeto utiliza um modelo de aprendizado de máquina para classificar estrelas com base em dados fornecidos no arquivo `star_classification.csv`. O script está escrito em Python e utiliza bibliotecas como pandas, TensorFlow e scikit-learn.

## Objetivo
O objetivo principal é treinar um modelo capaz de classificar estrelas em diferentes categorias com base em características específicas fornecidas no conjunto de dados. O modelo é treinado usando uma rede neural implementada com TensorFlow.

## Pré-processamento de Dados
O script inicia carregando o conjunto de dados `star_classification.csv` usando a biblioteca pandas. Em seguida, realiza algumas operações de pré-processamento, incluindo a remoção de colunas desnecessárias e a normalização dos dados.

## Modelo de Rede Neural
O modelo é uma rede neural simples com uma camada de entrada, uma camada oculta e uma camada de saída. A arquitetura da rede é a seguinte:

- **Camada de Entrada:** Número de neurônios igual ao número de características no conjunto de dados (16 neste caso).
- **Camada Oculta:** 10 neurônios com função de ativação ReLU e uma camada de dropout para evitar overfitting.
- **Camada de Saída:** 3 neurônios, correspondendo às classes de estrelas, usando a função de ativação softmax.
  
O otimizador Adam é utilizado para minimizar a função de custo, que é a entropia cruzada softmax.

## Treinamento do Modelo
O conjunto de dados é dividido em conjuntos de treinamento e teste. O modelo é treinado utilizando o conjunto de treinamento, e a acurácia é avaliada no conjunto de teste ao longo das épocas de treinamento.

## Parâmetros
- **Taxa de Aprendizado:** 0.001
- **Épocas:** 500
- **Tamanho do Lote (Batch Size):** 50

## Execução do Script
O script pode ser executado em um ambiente como o Google Colab. Certifique-se de ter todas as bibliotecas necessárias instaladas. O script imprime o custo médio durante o treinamento e a acurácia no conjunto de teste para cada época.

Certifique-se de ajustar o código conforme necessário, incluindo o caminho para o arquivo `star_classification.csv`, se não estiver no mesmo diretório do script.
