# ENEM-2023---EDA & Machine Learning
## Análise de dados ENEM 2023

### Este projeto tem como objetivo fazer o ELT, EDA e Machine Learning dos dados do ENEM 2023

### A ordem de leitura desse projeto é 
- Pré_Processamento_Parte1
- Pré_Processamento_Parte2
- Pré_Processamento_Parte3
- EDA
- Machine Learning

#### O processo de ETL (Extract, Transform, Load) começou com a coleta dos dados oficiais do ENEM 2023 no prórpio site "https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enem", e a parte "TL" foi desenvolvida nos notebooks 
- Pré_Processamento_Parte1
- Pré_Processamento_Parte2
- Pré_Processamento_Parte3

#### Durante a etapa de EDA foram analisados diversos aspectos de distribuição e análise entre as notas e fatores socioeconômicos

#### Durante a etapa de Machine Learning o objetivo é prever a média geral do estudante. Foram testados os seguintes modelos
- Regressão Linear
- Random Forest
- XGBoost Regressor

## Detalhamentos das Etapas:
## Pré Processamento

#### Um dos aspectos mais importantes de um ETL bem feito é **redução de memória RAM e em disco**. Já na primeira etapa de pré processamento, conseguimos uma redução de 82% e 84% respectivamente.

![image](https://github.com/user-attachments/assets/8a332224-4733-48c3-98d2-c3753c06e704)


#### Durante esses três notebooks foram realizadas as seguintes etapas:

- Otimização dos tipos de coluna com o auxílio da biblioteca 'dtype_diet' 
- Passar o dataframe com os tipos otimizados para o formato parquet
- Análise de percentual de nulos em cada coluna 
- Escolha das colunas a serem mantidas na análise
- Renomear as colunas do questionário para nomes mais intuitivos
- Criar um dataframe numérico, aplicando o eequivalente a um Ordinal Enconder
- Transformar as colunas categóricas que estão como numéricas, em colunas de fato categóricas
- Criar um dataframe categórico com os mapeamentos
- Divisão em dados de treino e teste

#### Durante a etapa de Pré_Processamento_Parte3 um detalhe importante foi a divisão em treino e teste de forma estratificada
<img width="600" alt="image" src="https://github.com/inesarruda/ENEM-2023---EDA-Machine-Learning/assets/112672449/84cc1e0a-4ca9-40a6-992d-89aa8cd1633c">

#### O resumo dos resultados das otimizações encontra-se no final do notebook

## EDA - Análise Exploratórioa de Dados
#### Durante a etapa de EDA queremos responder as analisar vários aspectos, dentre eles:
- Média geral das notas por tipo de escola (pública e privada)
  
    ![image](https://github.com/user-attachments/assets/66016795-ae6c-42cb-8740-ff3c676ab0bb)

- Média geral das notas por renda familiar

  ![media_por_renda](https://github.com/user-attachments/assets/47a53fe4-0941-4893-81fe-333f2edd1e98)

Esses foram apenas alguns exemplos, mas uma análise muito mais completa está presente no notebook "EDA"

## Machine Learning 

#### Nessa etapa foram feitas análises individuais dos modelos, e também um pipeline de dados com os pre processamentos necessários, exemplo:
![image](https://github.com/user-attachments/assets/ec54d05d-3f29-4eef-b33c-f74d021bfe25)

![image](https://github.com/user-attachments/assets/7698881c-7ce8-41ed-97c1-21ac08de6ce5)

### Conclusões:

#### Um dos principais aspectos desse projeto foi a limpeza de dados eficiente, como redução de memória RAM de 9,6 GB para 1,71 GB, e redução de 80% do espapaço em disco.

#### Também foi possível fazer uma análise de dados bem completa, mas com margem para explorar ainda mais nas próximas atualizações

#### Na etapa de Machine Learning obtivemos um bom resultado, mas assim como EDA, com margem para explorar ainda mais nas próximas atualizações.

### Perspectivas:
#### Durante o processo alguns passos ficaram para uma "Versão 2.0" como:
- Agrupar os estados em suas regiões e aplicar as análises comparando cada uma delas
- Fazer testes de hipótese em algumas premissas de nota e situação social
- Testar novos modelos 
- Fazer uma otimização de hiperparâmetros utilizando Bayseian Search ou Outros Métodos
- Fazer Feature Selection com outros métodos, como "Permutaion Importance"
- Verificar a possibilidade de colocar todos os arquivos no repositório com o git lgs

### Observações:
#### Os arquivos dos microdados do ENEM são muito grande e superam o limite de 100mb, numa próxima atualização vou verificar se funciona colocar todos os arquivos com o git lgs, mas todos os arquivos parquet criados e utilizados no pré processamento vem a partir do arquivo de origem 'MICRODADOS_ENEM_2023.csv' obtido no link "https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enem". 

