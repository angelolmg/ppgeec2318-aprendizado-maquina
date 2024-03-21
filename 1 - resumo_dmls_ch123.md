### **UNIVERSIDADE FEDERAL DO RIO GRANDE DO NORTE**

#### **PROGRAMA DE PÓS-GRADUAÇÃO EM ENGENHARIA ELÉTRICA E COMPUTAÇÃO**

#### **DEPARTAMENTO DE ENGENHARIA DA COMPUTAÇÃO E AUTOMAÇÃO**

  

**PPGEEC2318** - APRENDIZADO DE MÁQUINA - T01 (2024.1 - 5T3456)

  

**DOCENTE:** IVANOVITCH M D DA SILVA

**DISCENTE:** ANGELO L M DE GOES - 20231003266

  

<br>

  

**ATIVIDADE 1:** pontos principais no livro "*Designing Machine Learning Systems*" de Chip Huyen (caps. 1, 2 & 3)

## **Capítulo 1: Visão Geral de Sistemas de Aprendizado de Máquina**

Este capítulo fornece uma visão geral do estado atual da aprendizagem de máquina (ML), destacando sua rápida expansão a partir de 2016, principalmente devido aos avanços em *deep learning*. A ML está sendo amplamente utilizada em várias áreas da vida cotidiana, como comunicação, recomendação e na obtenção de informações, e há um potencial significativo para sua aplicação em diversas áreas como saúde, transporte, etc.

  

É crucial compreender que a **ML não é uma solução universal para todos os problemas** e que pode não fornecer necessariamente as soluções ótimas. Os engenheiros devem se questionar se o uso de ML é necessário e se é justificável em termos de custo-benefício dependendo da aplicação.

  
  
  

>  *Para tanto, podemos dizer que em essência a ML é uma abordagem para extrair padrões complexos de dados existentes e aplicar esses padrões para fazer previsões em novos dados.*

  
  
  

O capítulo também explora como a ML é mais comumente aplicada na indústria, em áreas como detecção de fraudes, otimização de preços, redução de custos, automação e análise de dados do cliente. Ao contrário do ambiente acadêmico, onde a precisão tende a ser a métrica principal, na indústria, o foco muitas vezes está no que efetivamente melhorar a eficiência dos processos e reduzir custos.

  

Além disso, o autor destaca que um sistema de **ML envolve outros aspectos além dos algoritmos, como a qualidade dos dados, implantação, monitoramento, manutenção e infraestrutura**. Estes são elementos críticos que precisam ser considerados ao aplicar ML no mundo real para garantir o sucesso das soluções implementadas.

## **Capítulo 2: Introdução ao Design de Sistemas de Aprendizado de Máquina**

 

Este capítulo explora a necessidade de alinhar os objetivos de sistemas de ML na indústria com as métricas que impulsionam este setor. Também enfatiza a importância da abundância de dados para o avanço desses sistemas ao longo da última década.

  

O autor ressalta a importância de **começar com os objetivos e requisitos do problema antes de empregar algoritmos de ML**, enquadrando-o como uma tarefa que a ML possa resolver. A abordagem MLOps é seguida, considerando o sistema de forma holística para garantir que todas as partes funcionem em conjunto para alcançar o objetivo, alinhado geralmente com a maximização dos lucros da indústria em questão.

  

Quatro requisitos principais são destacados: **confiabilidade** (o sistema deve manter o desempenho mesmo diante de adversidades como falhas humanas ou digitais), **escalabilidade** (capacidade de aumentar ou reduzir em escala), **manutenibilidade** (documentação, versionamento, reproducibilidade) e **adaptabilidade** (permitindo atualizações sem interrupção geral dos serviços).

  

De acordo com o autor:

  

>  *Desenvolver um sistema de ML é um processo iterativo e, na maioria dos casos, nunca termina. Uma vez que um sistema é colocado em produção, ele precisará ser continuamente monitorado e atualizado.*

  

Em termos gerais, as tarefas em ML podem envolver resolver **problemas de classificação** (onde a saída é uma classe) **ou de regressão** (onde a saída é um valor contínuo). Para treinar os modelos que resolvem estes problemas, empresas têm focado em especial na quantidade e qualidade dos seus dados, uma abordagem *data-over-mind*. Apesar de dados serem essenciais, pesquisadores mostram preocupação com este tipo de abordagem “data centrica”.

  

## **Capítulo 3: Fundamentos da Engenharia de Dados**
  

Este capítulo se concentra na **coleta, processamento, armazenamento** (utilizando motores de banco de dados), **recuperação e transferência de dados** em vários contextos e entre diferentes serviços.

  

O autor destaca diferentes fontes de dados, como **registros (logs), bancos de dados internos e dados de terceiros**. Uma vez coletados, os dados passam por processamento e são armazenados. A "serialização" converte os dados em um padrão utilizável, com formatos comuns incluindo **JSON, CSV** (formato de texto), **Pickle e Parquet** (formato binário), entre outros. Os formatos textuais são legíveis, enquanto os binários são mais compactos, embora ilegíveis.

  

Modelos de dados descrevem a representação dos dados, com destaque para os **modelos relacionais** (tabelas com relacionamentos/chaves) e os **modelos NoSQL** (documentos e grafos). SQL é a linguagem de consulta mais comumente usada para recuperar dados em modelos relacionais.

  

Há dois principais tipos de processamento: **transacional/OLTP** (otimizado para baixa latência e alta disponibilidade) e **analítico/OLAP** (otimizado para consultas analíticas). O processo ETL (Extração, Transformação, Carga) envolve extrair dados, transformá-los em um formato específico e carregá-los em um banco de dados. Os dados podem fluir entre processos por meio de bancos de dados, serviços tipo REST API e transporte em tempo real (por exemplo, Apache Kafka).

  

Depois de armazenados, os dados podem ser processados em lotes, gerando atributos estáticos, enquanto os dados transportados em tempo real são processados por motores de computação de *streaming*, gerando atributos dinâmicos.
