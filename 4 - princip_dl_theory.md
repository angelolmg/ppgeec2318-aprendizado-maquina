
﻿**UNIVERSIDADE FEDERAL DO RIO GRANDE DO NORTE**

#### **PROGRAMA DE PÓS-GRADUAÇÃO EM ENGENHARIA ELÉTRICA E COMPUTAÇÃO**

#### **DEPARTAMENTO DE ENGENHARIA DA COMPUTAÇÃO E AUTOMAÇÃO**

  

**PPGEEC2318** - APRENDIZADO DE MÁQUINA - T01 (2024.1 - 5T3456)

  

**DOCENTE:** IVANOVITCH M D DA SILVA

**DISCENTE:** ANGELO L M DE GOES - 20231003266

  

<br>

  

**ATIVIDADE 4:** Realizar uma análise aprofundada do capítulo 0 (zero) do livro "*The Principles of Deep Learning Theory*" disponível em https://arxiv.org/pdf/2106.10165.pdf.

---

O capítulo discute os princípios fundamentais da teoria de *deep learning*, destacando sua estrutura, funcionamento e, especialmente, **como seria possível formular princípios que permitam a análise teórica de redes relevantes**. Um ponto crucial é a concepção de que uma rede neural é essencialmente uma receita para calcular uma função parametrizada $f(x, \theta)$ utilizando unidades computacionais chamadas **neurônios**.

  

Esses neurônios processam os sinais de entrada por meio de conexões ponderadas e limiares de ativação para gerar uma saída. Em vez de serem programadas para resolver problemas diretamente, **as redes neurais são treinadas com dados do mundo real e assim aprendem a resolver determinados problemas**. Por sua vez, redes neurais profundas possuem múltiplos neurônios organizados em paralelo e em camadas sequenciais, com o objetivo de aprender representações incrementalmente refinadas do mundo, informação que pode ser usada para solucionar tarefas ainda mais complexas.

  

Além disso, o capítulo explora a importância de compreender as **propriedades macroscópicas** de redes grandes, mas com largura finita, para obter uma descrição teórica eficaz de redes profundas. Há uma analogia com a física, domínio da ciência que obteve grande sucesso na modelagem de sistemas complexos com múltiplos componentes; a termodinâmica, por exemplo, surge como um esforço para explicar a inovação do motor a vapor, que antes era visto como uma "caixa preta".

  

Após esforços de Maxwell, Boltzmann e Gibbs, as leis termodinâmicas emergem de suas observações meticulosas dos aspectos macroscópicos empíricos da máquina, por meio de uma abordagem conhecida como **teoria efetiva**. Foram essas previsões teóricas derivadas da mecânica estática do sistema que levaram, em última instância, ao consenso científico geral de que a matéria é composta de átomos e moléculas.

  

Assim, embora o entendimento microscópico das redes neurais seja evidente, compreender o macroscópico, ou seja, como uma rede computa uma função específica em vez de outra, representa o verdadeiro desafio: **entender os tipos de regularidades que surgem das propriedades estatísticas dessas grandes e profundas redes**. Ao abstrair os intricados detalhes dos componentes individuais dentro do sistema e, em vez disso, concentrar-se no comportamento coletivo do sistema como um todo, **teorias efetivas oferecem uma compreensão mais intuitiva de fenômenos complexos**. Essa abordagem permite aos pesquisadores capturar as propriedades essenciais e dinâmicas de um sistema sem se perder nas complexidades de cada componente individual.


Entretanto, a abordagem da teoria efetiva enfrenta desafios significativos ao ser aplicada às redes neurais profundas. A complexidade dessas redes, com suas múltiplas camadas e conexões intricadas, **dificulta a tradução direta de modelos teóricos simplificados para aplicações práticas**. Essa dificuldade pode requerer adaptações e considerações adicionais para garantir a relevância e eficácia prática desses modelos. Uma estratégia interessante explorada no capítulo, por exemplo, é pelo **truncamento** de derivadas de alta ordem, pelo **princípio da esparcidade**. Isto simplifica massivamente os cálculos para uma função essencialmente infinita, no entanto é inconclusivo o quanto essa simplificação geraria uma incompatibilidade entre descrição teórica e observação prática.


Dessa maneira, apesar de ser uma estratégia efetiva, pela complexidade do problema em questão, se torna essencial explorar medidas que combinem a simplicidade da teoria efetiva com a complexidade das redes neurais profundas, visando desenvolver modelos teóricos mais robustos e aplicáveis. Superar esses desafios requer uma abordagem cuidadosa e iterativa que leve em conta tanto a compreensão teórica quanto a aplicação prática dessas teorias no contexto do aprendizado profundo.
