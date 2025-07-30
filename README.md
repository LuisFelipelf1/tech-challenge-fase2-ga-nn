
# Tech Challenge - FIAP (Fase 2)

## 🎯 Desafio
Desenvolver um sistema baseado em Algoritmo Genético para otimizar a arquitetura de uma **Rede Neural Artificial**, com o objetivo de maximizar a acurácia em um problema de classificação.

---

## 🧪 Problema Escolhido
**Otimizar a estrutura de uma rede neural para o dataset Iris.**

Cada indivíduo da população representa uma configuração de rede com:
- Número de neurônios na primeira camada oculta
- Número de neurônios na segunda camada oculta
- Função de ativação da camada 1
- Função de ativação da camada 2

Exemplo de gene:
```python
[32, 16, 0, 1]  # 32 neurônios + ReLU, depois 16 neurônios + Sigmoid
```

As ativações possíveis são:
- 0 = relu
- 1 = sigmoid
- 2 = tanh

---

## ⚙️ Implementação

- **Linguagem**: Python
- **Bibliotecas**: `tensorflow.keras`, `sklearn`, `numpy`, `random`
- **Fitness**: acurácia da rede neural treinada por 30 épocas
- **Dataset**: Iris (sklearn.datasets)
- **GA**: Seleção dos melhores, crossover e mutação

---

## 📈 Análise dos Resultados

O algoritmo genético conseguiu encontrar boas configurações de rede em poucas gerações.  
Em geral, as melhores redes possuíam:
- Camadas ocultas com 16 a 48 neurônios
- Funções de ativação ReLU ou combinação ReLU + Sigmoid

A acurácia final média das melhores redes ficou entre **95% e 98%**, superando configurações manuais simples.  
As configurações eram avaliadas automaticamente, e a seleção natural foi eficiente para otimizar a rede sem intervenção manual.

---

## 🧠 Conclusão Crítica

Este projeto mostrou que **algoritmos genéticos são eficazes para otimização de arquitetura de redes neurais** em problemas simples como o Iris.  
Apesar da simplicidade do dataset, o processo evolutivo é facilmente adaptável para bases maiores.

### Pontos fortes:
- Automatização da escolha de hiperparâmetros
- Resultados concretos e interpretáveis
- Código reutilizável para outros datasets

### Limitações:
- Tempo de execução cresce com o número de épocas e tamanho da população
- A solução pode ser sensível a valores iniciais e aleatoriedade

Este tipo de abordagem pode ser útil em cenários reais onde **não é viável testar manualmente dezenas de combinações**.  
Mesmo com redes simples, o GA se mostrou uma ferramenta poderosa para aprender boas estruturas.

---

## 📁 Entregáveis
- Código-fonte (notebook)
- Vídeo com demonstração no YouTube
- Este README explicando o projeto

---

## 👤 Autor
**Luís Felipe Alves Silva**  
RM: 363734  
Pós-graduação em Inteligência Artificial para Devs – FIAP
