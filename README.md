# 🏃‍♂️ Análise de Desempenho em Ultramaratonas no Brasil: Foco em Corridas de 50 km 🏆

<p align="center">
  <a href="https://github.com/Edu-png">
    <img src="https://img.shields.io/badge/Autor-Eduardo%20Coqueiro-purple?style=flat&logo=github" alt="Autor">
  </a>
  <a href="mailto:eduardocoqueiro@gmail.com">
    <img src="https://img.shields.io/badge/Email-eduardocoqueiro%40gmail.com-purple?style=flat&logo=gmail" alt="Email">
  </a>
  <a href="https://linkedin.com/in/eduardocoqueiro/">
    <img src="https://img.shields.io/badge/LinkedIn-Eduardo%20Coqueiro-purple?style=flat&logo=linkedin" alt="LinkedIn">
  </a>
  <a href="https://kaggle.com/EduardoCoqueiro">
    <img src="https://img.shields.io/badge/Kaggle-Eduardo%20Coqueiro-blue?style=flat&logo=kaggle" alt="Kaggle">
  </a>
</p>

![CAPAS - PROJETOS (4)](https://github.com/user-attachments/assets/e99fa333-46c5-498e-b16a-984a104c12a8)

---

## 📌 Sumário

1. [📚 Introdução](#-introdução)
2. [🎯 Objetivos do Projeto](#-objetivos-do-projeto)
3. [🛠 Metodologia](#-metodologia)
4. [📊 Resultados e Conclusões](#-resultados-e-conclusões)
   - [1. Distribuição da Velocidade Média](#1-distribuição-da-velocidade-média)
   - [2. Diferenças de Desempenho por Gênero](#2-diferenças-de-desempenho-por-gênero)
   - [3. Relação entre Idade e Velocidade Média](#3-relação-entre-idade-e-velocidade-média)
   - [4. Impacto da Sazonalidade](#4-impacto-da-sazonalidade)
   - [5. Desempenho por Gênero e Estação](#5-desempenho-por-gênero-e-estação)
   - [6. Relação entre Número de Participantes e Velocidade Média](#6-relação-entre-número-de-participantes-e-velocidade-média)
   - [7. Comparação por Nacionalidade](#7-comparação-por-nacionalidade)
   - [8. Destaque para o Brasil](#8-destaque-para-o-brasil)
   - [9. Tendências ao Longo dos Anos](#9-tendências-ao-longo-dos-anos)
   - [10. Eventos com Maior Velocidade Média](#10-eventos-com-maior-velocidade-média)
5. [👏 Agradecimentos](#-agradecimentos)
6. [📞 Contato](#-contato)

## 📚 Introdução

Este projeto nasceu da minha paixão por esportes de resistência e do desejo de aplicar análises avançadas de dados em eventos de ultramaratona. Utilizando um dataset disponível no Kaggle, focamos nas corridas de 50 km realizadas no Brasil, investigando como diferentes variáveis, como gênero, idade e sazonalidade, impactam o desempenho dos atletas.

O dataset original pode ser encontrado em: [Kaggle Dataset](https://www.kaggle.com/datasets/aiaiaidavid/the-big-dataset-of-ultra-marathon-running).

---

## 🎯 Objetivos do Projeto

Este projeto busca atingir os seguintes objetivos:

1. **Entender diferenças de desempenho entre gêneros:**
   - Analisar as velocidades médias alcançadas por homens e mulheres, comparando distribuições e identificando possíveis disparidades de desempenho em corridas de 50 km.

2. **Identificar o impacto da idade no desempenho:**
   - Mapear as faixas etárias com maior e menor desempenho, avaliando a relação entre idade, preparo físico e experiência nas corridas de longa distância.

3. **Avaliar o efeito da sazonalidade:**
   - Explorar como as estações do ano influenciam o desempenho dos atletas, considerando variáveis como clima e condições ambientais específicas.

4. **Investigar tendências temporais:**
   - Analisar o desempenho dos atletas ao longo dos anos para identificar padrões ou mudanças no perfil dos participantes e na organização dos eventos.

5. **Comparar desempenho entre nacionalidades:**
   - Avaliar como atletas de diferentes países se comportam em corridas realizadas no Brasil, destacando possíveis diferenças de preparo e estratégia.

6. **Examinar a relação entre número de participantes e desempenho:**
   - Entender se eventos com maior número de participantes apresentam diferenças significativas de desempenho médio em comparação a eventos menores.

7. **Fornecer insights práticos:**
   - Gerar informações úteis para atletas, treinadores e organizadores de eventos sobre como fatores demográficos e ambientais podem ser utilizados para melhorar o desempenho ou planejar corridas.

---

## 🛠 Metodologia

A análise do dataset de ultramaratonas foi conduzida de maneira sistemática, seguindo as etapas abaixo. Cada passo foi cuidadosamente planejado para garantir a qualidade dos dados e obter insights significativos.

### 1. **Importação e Limpeza de Dados**
   - **Importação dos Dados:** 
     - Os dados foram carregados a partir de um dataset disponível no Kaggle, utilizando a biblioteca `pandas` para manipulação.
   - **Remoção de Valores Nulos:**
     - Foram eliminados registros com informações ausentes, como datas inválidas e valores faltantes em colunas essenciais.
   - **Correção de Tipos de Dados:**
     - Ajuste de colunas para tipos apropriados, como conversão de datas para o formato `datetime` e transformação de valores numéricos para `float` ou `int`.

### 2. **Tradução e Modificação de Colunas**
   - As colunas originais em inglês foram traduzidas para o português para maior acessibilidade.
   - Colunas novas foram criadas para enriquecer a análise:
     - **Idade do atleta:** Calculada com base no ano de nascimento e no ano do evento.
     - **Estação do ano:** Determinada a partir da data do evento, categorizando como Verão, Outono, Inverno ou Primavera.
     - **País do evento:** Extraída do nome do evento.

### 3. **Recorte de Dados**
   - **Foco em Corridas de 50 km:** 
     - Seleção de eventos com distância específica de 50 km.
   - **Limitação Geográfica:**
     - Filtragem para incluir apenas eventos realizados no Brasil, criando o conjunto de dados `run_BRA`.

### 4. **Análise Exploratória de Dados (EDA)**
   - **Distribuições e Estatísticas:**
     - Visualização da distribuição da velocidade média dos atletas utilizando gráficos como histogramas e gráficos violino.
     - Cálculo de médias, medianas e dispersões para identificar padrões.
   - **Análise Comparativa:**
     - Comparação de velocidade média entre gêneros, idades e estações do ano.
   - **Correlação entre Variáveis:**
     - Gráficos de dispersão com regressão para explorar relações entre idade e velocidade média, além de comparações de desempenho ao longo dos anos.

### 5. **Visualizações**
   - **Gráficos Interativos e Informativos:**
     - Histogramas, gráficos de barras, violinos e de linha foram criados para visualizar padrões e tendências.
   - **Destaques Específicos:**
     - Inclusão de destaques para a performance brasileira em relação a outros países.

### 6. **Extração de Insights**
   - Cada análise foi conduzida para responder perguntas específicas, como:
     - Diferenças de velocidade média entre gêneros.
     - Impacto da estação do ano no desempenho.
     - Tendências ao longo do tempo.

### 7. **Ferramentas Utilizadas**
   - **Linguagem de Programação:** Python.
   - **Bibliotecas:**
     - `pandas` para manipulação e limpeza de dados.
     - `numpy` para cálculos estatísticos.
     - `seaborn` e `matplotlib` para criação de gráficos e visualizações.

### 8. **Exportação de Resultados**
   - Os dados tratados foram exportados para arquivos CSV para permitir análises futuras ou integração com ferramentas de visualização mais avançadas, como Power BI ou Tableau.

---

## 📊 Resultados e Conclusões

Nesta seção, detalhamos os principais resultados da análise e as conclusões extraídas, acompanhadas de gráficos representativos.

---

### 1. Distribuição da Velocidade Média

O gráfico de distribuição mostra a concentração de velocidades médias em corridas de 50 km realizadas no Brasil. A maioria dos atletas mantém velocidades entre 6 e 8 km/h, representando um ritmo consistente para provas de longa distância. 

![g1](https://github.com/user-attachments/assets/5efced3c-855e-4a03-9301-144996cdf10c)

---

### 2. Diferenças de Desempenho por Gênero

A análise revelou que os homens possuem velocidades médias superiores às mulheres em todas as faixas, com uma diferença significativa nas velocidades mais altas. Isso pode ser explicado por diferenças fisiológicas e proporção de participantes.

![g2](https://github.com/user-attachments/assets/bd63f584-cbc2-413c-84cf-be2c0ed4a63b)

---

### 3. Relação entre Idade e Velocidade Média

Atletas entre 40 e 60 anos tendem a apresentar melhores velocidades médias, indicando o papel da experiência e preparação em corridas longas. A performance diminui levemente após os 70 anos.

![g3](https://github.com/user-attachments/assets/de400e53-e076-4fcf-9dab-4a155e75f90c)

---

### 4. Impacto da Sazonalidade

A estação do ano afeta significativamente o desempenho dos atletas. O verão apresentou as maiores velocidades médias, enquanto a primavera foi a estação com menor desempenho médio.

![g4](https://github.com/user-attachments/assets/286d40eb-9ae0-43e6-a77f-2b1b3e159d14)

---

### 5. Desempenho por Gênero e Estação

Homens e mulheres seguem o mesmo padrão de sazonalidade, com ambos apresentando melhores desempenhos no verão. No entanto, a diferença de velocidade entre os gêneros permanece evidente em todas as estações.

![g5](https://github.com/user-attachments/assets/32f18e5d-6d90-46a1-9d5b-4573cce403a1)

---

### 6. Relação entre Número de Participantes e Velocidade Média

Eventos com menos participantes tendem a apresentar velocidades médias mais altas, enquanto grandes eventos mostram maior variabilidade nos desempenhos.

![g6](https://github.com/user-attachments/assets/dfdeff17-36f5-4ba9-b2b2-857656d014b3)

---

### 7. Comparação por Nacionalidade

Atletas de diferentes países apresentam variabilidade significativa em suas velocidades médias, destacando possíveis diferenças em treinamento e preparo físico.

![g7](https://github.com/user-attachments/assets/6496628b-03f8-4460-86dd-163098d1876e)

---

### 8. Destaque para o Brasil

Ao destacar a performance dos atletas brasileiros, observamos que, embora estejam em posição competitiva intermediária, apresentam consistência em eventos nacionais.

![g8](https://github.com/user-attachments/assets/381bc1cf-809a-4574-a6ae-147b9c0e89ee)

---

### 9. Tendências ao Longo dos Anos

Analisando as velocidades médias ao longo dos anos, identificamos um declínio inicial seguido por oscilações, sugerindo mudanças no perfil dos participantes ou nas condições dos eventos.

![g9](https://github.com/user-attachments/assets/dcb06894-96bd-451c-95f0-21d8f4ebea5d)

---

### 10. Eventos com Maior Velocidade Média

Os eventos com maior velocidade média geralmente apresentam características específicas, como alta competitividade, boa organização e condições climáticas favoráveis.

![g10](https://github.com/user-attachments/assets/6659e0a9-52d3-437d-b6fe-a7a16e07bdaa)

---

### Considerações Finais

- **Insights Relevantes:**
  - Diferenças claras de desempenho entre gêneros, idades e estações do ano.
  - Impacto do número de participantes no desempenho médio.
  - Destaques nacionais que reforçam a competitividade do Brasil em eventos locais.

- **Próximos Passos:**
  - Expansão da análise para incluir outros fatores, como altimetria das rotas.
  - Integração com dados climáticos mais detalhados para aprofundar o impacto da sazonalidade.
  - Buscar um data-set de 5 e 10 km para comparar com os meus próprios resultados!

---

## 👏 Agradecimentos

Gostaria de expressar minha gratidão ao **Kaggle** por disponibilizar o dataset utilizado neste projeto, permitindo uma análise aprofundada e prática sobre corridas de ultramaratona. A estrutura e a riqueza do dataset foram fundamentais para extrair insights relevantes e aplicáveis.

Além disso, agradeço à comunidade de análise de dados e desenvolvedores por compartilhar conhecimento e ferramentas, como as bibliotecas `pandas`, `matplotlib` e `seaborn`, que viabilizaram a manipulação e visualização dos dados.


<div align="center">
  <img src="https://github.com/user-attachments/assets/54afb33c-97be-40b6-8c96-0f12852e946f" alt="thank-you" width="500">
</div>

## 📞 Contato
- **LinkedIn:** [Eduardo Coqueiro](https://www.linkedin.com/in/eduardocoqueiro/)
- **Site:** [Eduardo Coqueiro](https://dataguy.my.canva.site/eduardo-coqueiro)
- **Kaggle:** [Eduardo Coqueiro](https://www.kaggle.com/eduardocoqueiro)



