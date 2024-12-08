# machine-learning-project

# 1. Introdução

Este projeto foi inicialmente concebido para explorar a interseção entre processamento de linguagem natural e geração de áudio, visando criar música a partir de descrições textuais detalhadas. A ideia era utilizar a base de dados MusicCaps, que fornece pares de texto e clipes musicais, para desenvolver um modelo capaz de traduzir nuances textuais em características musicais, como gênero, humor e ritmo. Apesar de inovadora, a abordagem apresentou desafios significativos em termos de processamento computacional e complexidade do modelo, levando-nos a reconsiderar o escopo do trabalho.

Dessa forma, decidimos redirecionar o foco para um problema prático e mais alinhado com nossos recursos: a análise de dados educacionais do ENEM (Exame Nacional do Ensino Médio). Essa nova proposta explora a identificação de padrões e a previsão de aprovação de alunos com base em informações contidas na base do ENEM e em dados históricos de notas de corte de nossa faculdade.

O ENEM é uma prova ampla e de grande importância no Brasil, servindo como porta de entrada para inúmeras universidades. A base de dados do exame oferece informações detalhadas sobre as questões, alternativas, assuntos abordados e características dos alunos que realizaram a prova. Com essa riqueza de informações, vislumbramos a oportunidade de aplicar técnicas de aprendizado de máquina para identificar agrupamentos (clusters) de estudantes, prever notas e simular aprovações de maneira eficiente.

A proposta atual visa não apenas uma aplicação prática de aprendizado de máquina no contexto educacional, mas também a criação de um modelo que possa ser escalado para auxiliar instituições de ensino na análise de desempenho de candidatos, potencializando processos seletivos e identificando oportunidades de melhorias pedagógicas.

---

# 2. Base de Dados

## 2.1 Base Inicial - MusicCaps

A MusicCaps é uma base de dados voltada para a geração de música a partir de descrições textuais e foi introduzida no artigo *"MusicLM: Generating Music From Text"*, de Agostinelli et al. A base é composta por 5,5 mil pares de música e texto, onde cada trecho musical de 10 segundos é acompanhado por uma descrição detalhada fornecida por especialistas humanos.

### 2.1.1 Características da Base MusicCaps

#### Descrições Textuais

- Para cada clipe musical, a base inclui uma legenda em texto livre, composta em média por quatro frases.  
- Essas legendas descrevem aspectos da música, incluindo sua estrutura emocional e técnica.  
- As descrições incluem informações como:  
  - **Gênero**: pop, rock, jazz.  
  - **Humor**: alegre, melancólica, introspectiva.  
  - **Tempo**: rápido, moderado, lento.  
  - **Vozes**: descrição das vozes.  
  - **Instrumentação**: guitarra, bateria, piano.  
  - **Dissonâncias**: tensões harmônicas.  
  - **Ritmo**: características rítmicas e métricas.

#### Formato de Análise e Aplicações

A estrutura rica da base facilita a análise de como descrições textuais complexas podem ser convertidas em música, oferecendo oportunidades para explorar influências do texto na composição musical.

### 2.1.2 Motivação e Desistência da Base MusicCaps

Apesar do potencial inovador da MusicCaps, a complexidade computacional exigida para implementar os modelos necessários nos levou a mudar o escopo do projeto.

---

## 2.2 Base Atual - ENEM

A nova base de dados escolhida é relacionada ao Exame Nacional do Ensino Médio (ENEM), uma das principais avaliações educacionais no Brasil.  

### 2.2.1 Descrição da Base ENEM

#### Fonte e Disponibilidade

- Base ENEM 2019 disponível no Kaggle.  
- Inclui dados demográficos, desempenho e informações educacionais.

#### Estrutura da Prova

- 180 questões objetivas divididas em quatro áreas:  
  - **Ciências Humanas**  
  - **Linguagens e Códigos**  
  - **Ciências da Natureza**  
  - **Matemática**

---

# 3. Sobre o Projeto

## 3.1 Objetivo do Projeto

Realizar uma análise de clusterização e prever a aprovação dos alunos com base na nota de corte histórica da faculdade.  

### Identificação de Clusters de Desempenho

- Utilizamos o algoritmo **K-means** para agrupar alunos com características semelhantes.  

### Previsão da Aprovação dos Alunos

- Modelo preditivo utilizando **árvores de decisão**.  
- Entrada: variáveis de desempenho e dados demográficos.  
- Saída: probabilidade de aprovação.  

---

## 3.3 Impacto Esperado

1. **Identificação de Padrões de Desempenho:**  
   - Suporte personalizado para alunos abaixo da média.  
   - Políticas inclusivas baseadas em fatores demográficos.  

2. **Otimização de Recursos Educacionais:**  
   - Investimentos estratégicos em programas e apoios direcionados.  

3. **Uso em Processos Seletivos:**  
   - Planejamento acadêmico e identificação de talentos.  
