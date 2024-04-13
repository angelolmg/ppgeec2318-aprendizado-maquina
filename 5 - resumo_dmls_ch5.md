
﻿**UNIVERSIDADE FEDERAL DO RIO GRANDE DO NORTE**

#### **PROGRAMA DE PÓS-GRADUAÇÃO EM ENGENHARIA ELÉTRICA E COMPUTAÇÃO**

#### **DEPARTAMENTO DE ENGENHARIA DA COMPUTAÇÃO E AUTOMAÇÃO**

  

**PPGEEC2318** - APRENDIZADO DE MÁQUINA - T01 (2024.1 - 5T3456)

  

**DOCENTE:** IVANOVITCH M D DA SILVA

**DISCENTE:** ANGELO L M DE GOES - 20231003266

  

<br>

  

**ATIVIDADE 5:** Elaborar um resumo detalhado do Capítulo 5 do Livro "*Designing Machine Learning Systems: An Iterative Process for Production-Ready Applications*" por Chip Huyen.


## 1. Estratégias e técnicas de engenharia de recursos

O capítulo aborda de forma abrangente a relevância de selecionar os recursos (ou características) apropriados para os modelos de aprendizado de máquina, além de discutir técnicas úteis e boas práticas nesse âmbito. A autora ressalta que **ter os recursos adequados pode resultar em um aumento significativo no desempenho em comparação com abordagens algorítmicas sofisticadas, como ajuste de hiperparâmetros**. Entre as principais estratégias destacadas, estão:

- **Utilização de características produzidas manualmente:**

Enquanto os modelos de aprendizado profundo podem extrair automaticamente características dos dados, o aprendizado de máquina tradicional muitas vezes requer que as características sejam produzidas manualmente. É crucial entender quando confiar em características aprendidas, que podem identificar padrões complexos nos dados, e quando utilizar características produzidas, que podem fornecer *insights* específicos do domínio não capturados por algoritmos automáticos de aprendizado.

Ao equilibrar o uso de características aprendidas e produzidas, os profissionais podem melhorar tanto o desempenho quanto a interpretabilidade do modelo. Por exemplo, na área de Processamento de Linguagem Natural (NLP), características úteis podem ser produzidas utilizando técnicas como *n-grams*. Esse processo inclui pré-processamento, que envolve a remoção de pontuação, lematização e tokenização para gerar características para análise textual.

- **Tratamento de valores ausentes:**

Lidar com valores ausentes é um desafio comum em conjuntos de dados do mundo real. O tratamento adequado de valores ausentes é essencial para evitar resultados enviesados ou imprecisos do modelo. Técnicas de imputação e exclusão podem ser empregadas com base na natureza dos dados faltosos e no impacto desses valores para o modelo. O tratamento de valores ausentes garante a integridade e confiabilidade do conjunto de dados, levando a modelos de aprendizado de máquina mais robustos.

- **Escalonamento:**

Escalonar características é crucial para garantir que todas as características contribuam igualmente para o processo de treinamento do modelo. Ao escalonar características para uma faixa semelhante, **os modelos podem convergir mais rapidamente e evitar serem dominados por características com magnitudes maiores**.

- **Discretização:**

A discretização envolve a conversão de características contínuas em intervalos ou categorias discretas. Esse processo pode ajudar a simplificar dados complexos, reduzir ruídos e melhorar a interpretabilidade do modelo. Ao discretizar características contínuas, os profissionais podem capturar relacionamentos e padrões não lineares que podem não ser evidentes nos dados contínuos originais.

- **Codificação de características categóricas:**

O capítulo aborda a transformação de características contínuas em características categóricas e explora a melhor forma de lidar com elas. Destaca-se que, embora muitas categorias sejam estáticas, algumas mudam ao longo do tempo, como marcas de produtos. Para resolver esse problema, é apresentada a técnica do "*hashing trick*", que **utiliza uma função de hash para atribuir um valor único a cada categoria, permitindo a codificação mesmo de categorias nunca antes vistas**. Essa abordagem, embora considerada "complicada" por alguns acadêmicos, é amplamente adotada na indústria devido à sua eficácia e é essencial em *frameworks* como Vowpal Wabbit, scikit-learn, TensorFlow e gensim.

- **Cruzamento de características:**

*Feature Crossing* é uma técnica que combina duas ou mais características para gerar novas características. **Isso é útil para modelar as relações não lineares entre as características**. Por exemplo, ao prever se alguém desejará comprar uma casa nos próximos 12 meses, pode-se suspeitar que haja uma relação não linear entre estado civil e número de filhos, então essas características são combinadas para criar uma nova característica "casamento e filhos". 

Embora o *feature crossing* ajude a modelar relações não lineares entre variáveis, é essencial para modelos que não conseguem aprender ou têm dificuldade em aprender relações não lineares, como regressão linear, regressão logística e modelos baseados em árvore.  Apesar disso, um cuidado que se deve ter é que esta técnica pode aumentar muito o número de características, o que requer mais dados para que os modelos aprendam todas esses possíveis valores, do contrario pode causar o *overfitting* do modelo aos dados de treino.

- **Codificação de posicionamento:**

A incorporação de posicionamento desempenha um papel fundamental no processamento de dados sequenciais, como no processamento de linguagem natural e na análise de séries temporais. Essa técnica representa a posição dos elementos (ou *tokens*) em uma sequência, capacitando os modelos a capturar dependências sequenciais e padrões temporais nos dados. Ao incluir essas informações de posicionamento, os modelos aprimoram sua capacidade de compreender e prever sequências com maior precisão.

## 2. Melhores práticas na engenharia de recursos

Na engenharia de características, é crucial adotar boas práticas para mitigar problemas comuns, como **vazamento de dados** (*data leakage*) e **overfitting**. O vazamento de dados ocorre quando informações da variável alvo influenciam inadvertidamente as características utilizadas para fazer previsões, resultando em um desempenho inflado durante o treinamento, mas uma baixa capacidade de generalização para novos dados durante a inferência. Identificar e evitar o vazamento de dados é essencial para construir modelos de aprendizado de máquina confiáveis.

Em exemplos reais dados pela autora, um modelo destinado a prever câncer de pulmão a partir de tomografias computadorizadas sofreu vazamento de dados ao depender inadvertidamente de informações sobre o *CT scanner* específico usado em um hospital. Essa correlação levou a um desempenho fraco quando testado em dados de outro hospital com um procedimento de escaneamento diferente. Outra instância de vazamento de dados foi observada em uma competição do Kaggle, onde os participantes reverteram os rótulos de teste a partir dos dados de treinamento, explorando um vazamento no processo de síntese de dados para obter uma vantagem injusta.

Com isso em mente, é fundamental evitar causas típicas de vazamento de dados, como o uso de informações futuras como características, a realização de etapas de pré-processamento de dados (como escalonamento ou codificação) antes de dividir os dados de treino, **incorporando implicitamente dados não disponíveis no momento da previsão**, como rótulos ou características derivadas desconhecidas em cenários do mundo real, tais como média e variância dos dados usados para treinamento. 

Também é crucial **avaliar a relevância das características em relação à variável alvo**, compreender os métodos de coleta e processamento de dados para identificar possíveis fontes de vazamento, normalizar os dados para mitigar discrepâncias entre as fontes, remover amostras duplicadas e envolver especialistas no assunto para oferecer *insights* sobre as práticas de coleta de dados e sugerir modificações nos dados para otimizar o desempenho em uma tarefa específica. Isso pode incluir o uso de técnicas como imputação, remoção e cruzamento de características. Tudo isso demanda uma compreensão profunda da geração e linhagem dos dados para garantir a qualidade e confiabilidade das características, bem como a atualização e remoção regular de características menos úteis para evitar dívidas técnicas e manter o desempenho do modelo.
