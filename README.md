# ETL e Data Warehouse com N8N – State of Data Brazil 2024/2025

## Sobre o Projeto

Este projeto foi desenvolvido como atividade prática do Módulo 2 do curso de Data Analytics, com foco na construção de um processo de ETL (Extract, Transform and Load) utilizando a ferramenta N8N.

O desafio consistiu em transformar os dados da pesquisa State of Data Brazil 2024/2025 em uma estrutura analítica baseada em Data Warehouse, possibilitando a análise de questões relacionadas ao mercado brasileiro de tecnologia e dados.

## Objetivos

* Construir um processo automatizado de ETL utilizando N8N;
* Realizar limpeza, transformação e enriquecimento dos dados;
* Implementar uma estrutura dimensional (Star Schema);
* Disponibilizar os dados para análises de negócio;
* Aplicar conceitos de Engenharia de Dados e Business Intelligence.

## Base de Dados

A base utilizada foi a pesquisa State of Data Brazil 2024/2025, disponibilizada pela comunidade Data Hackers.

Fonte:
https://www.kaggle.com/datasets/datahackers/state-of-data-brazil-20242025

## Problemas de Negócio Analisados

### 1. Desigualdade Regional no Mercado de Tecnologia

Investigar se profissionais residentes fora do eixo Sul-Sudeste possuem menor acesso a oportunidades de emprego, progressão de carreira e aprovação em processos seletivos.

**Questões analisadas:**

* Quantidade de oportunidades de emprego recebidas por região;
* Aprovação em processos seletivos;
* Velocidade de progressão de carreira;
* Comparação entre Sudeste, Sul, Nordeste, Norte e Centro-Oeste.

### 2. Equidade Salarial e Pay Gap

Avaliar possíveis diferenças salariais entre profissionais com características demográficas distintas.

**Questões analisadas:**

* Distribuição salarial por gênero;
* Distribuição salarial por raça;
* Análise interseccional entre gênero e raça;
* Comparação entre profissionais de mesmo nível de senioridade.

### 3. Burnout e Saúde Mental

Investigar a relação entre características demográficas e percepção de estresse no ambiente de trabalho.

**Questões analisadas:**

* Nível de cobrança e estresse por gênero;
* Nível de cobrança e estresse por raça;
* Nível de cobrança e estresse por faixa etária;
* Nível de cobrança e estresse para pessoas com deficiência (PCD).

## Arquitetura da Solução

O projeto foi desenvolvido seguindo o fluxo abaixo:

1. Extração dos dados da pesquisa;
2. Tratamento e padronização dos dados;
3. Modelagem dimensional do Data Warehouse;
4. Carga das tabelas de dimensão;
5. Carga da tabela fato;
6. Disponibilização dos dados para análises.

## Modelo Dimensional

Foi adotada a metodologia Star Schema (Modelo Estrela), composta por três dimensões e uma tabela fato central.

### Dimensão Demográfica (dim_demografica)

Armazena informações relacionadas ao perfil dos participantes.

**Atributos:**

* Idade
* Faixa etária
* Gênero
* Cor/Raça/Etnia
* Indicador PCD

### Dimensão Localização (dim_localizacao)

Armazena informações geográficas dos participantes.

**Atributos:**

* UF
* Região

### Dimensão Carreira (dim_carreira)

Armazena informações profissionais dos participantes.

**Atributos:**

* Nível profissional
* Faixa salarial

### Fato Resposta Pesquisa (fato_resposta_pesquisa)

Tabela responsável por armazenar as métricas utilizadas nas análises.

**Métricas:**

* Quantidade de oportunidades recebidas;
* Aprovação em processos seletivos;
* Velocidade de progressão de carreira;
* Nível de cobrança e estresse no trabalho.

## Tecnologias Utilizadas

* N8N
* PostgreSQL
* SQL
* Data Warehouse
* GitHub

## Estrutura do Repositório

```text
├── README.md
├── Documentacao
│   └── Documentacao.pdf
├── N8N
    └── workflow.json
```

## Resultados Esperados

A solução desenvolvida permite analisar indicadores relacionados à desigualdade regional, equidade salarial e saúde mental dos profissionais de dados brasileiros, fornecendo informações relevantes para empresas, profissionais de Recursos Humanos, áreas de Remuneração e Benefícios, iniciativas ESG e formuladores de políticas públicas.

## Autor(es)

Projeto desenvolvido por Helena Ferreira, João Luiz Sampaio e João Neto como atividade prática do Módulo 2 de ETL.

