# Índice

## SAS

1. [Explorando os dados](#explorando-os-dados)  
    1.1. [Declaração das bibliotecas](#declaracao-das-bibliotecas)  
    1.2. [Checagem das bases](#checagem-das-bases)  
    1.3. [Uma forma de organizar Datas](#uma-forma-de-organizar-datas)

2. [Visualizando Frequências](#visualizando-frequencias)  
    2.1. [Relatórios de Frequências](#relatorios-de-frequencias)  
    2.2. [Criação de uma nova variável](#criacao-de-uma-nova-variavel)

3. [Continuando com Frequências](#continuando-com-frequencias)  
    3.1. [Frequências cruzadas](#frequencias-cruzadas)  
    3.2. [Continuando com Frequências cruzadas](#continuando-com-frequencias-cruzadas)  
    3.3. [Em busca de chave única](#em-busca-de-chave-unica)  
    3.4. [Comentários e Salvar a Base](#comentarios-e-salvar-a-base)

4. [Trabalhando com problemas na base](#trabalhando-com-problemas-na-base)  
    4.1. [Ausências de informações](#ausencias-de-informacoes)  
    4.2. [Múltiplos Filtros](#multiplos-filtros)  
    4.3. [Múltiplos condicionais](#multiplos-condicionais)  
    4.4. [Corrigindo os Missings](#corrigindo-os-missings)  
    4.5. [Conectando e salvando a base](#conectando-e-salvando-a-base)

5. [Introdução aos formatos](#introducao-aos-formatos)  
    5.1. [Obtendo estado a partir do CEP](#obtendo-estado-a-partir-do-cep)  
    5.2. [Formato e tamanho](#formato-e-tamanho)  
    5.3. [Subtexto](#subtexto)  
    5.4. [Convertendo um texto em número](#convertendo-um-texto-em-numero)

6. [Usando formatos personalizados](#usando-formatos-personalizados)  
    6.1. [Como agilizar processos](#como-agilizar-processos)  
    6.2. [Formatos personalizados](#formatos-personalizados)  
    6.3. [Usando formatos a nosso favor](#usando-formatos-a-nosso-favor)  
    6.4. [Conectar e salvar](#conectar-e-salvar)

---
Sas é um software muito usado em mercado financeiro podendo trazer informações úteis para tomadas de decisões.
Você pode acessar o sas pelo link [SAS](https://www.sas.com/pt_br/home.html)

## Explorando os dados

Exportando dados para SAS

### Declaração das bibliotecas

#### DATASETS

| COMANDO | DESCRICAO |
|--------|------------|
| PROC   | comando inicial para rodar querys |
| RUN   | para finalizar a querys |
| DATASETS | para rodar um dataset e mostrar alguns detalhes |
| LIBNAME | para declarar um nome de uma biblioteca e usar seu conteúdo |
| PRINT | retorna todos valores em um dataset como a sua tabela geral |
| CONTENT | mostra detalhes mais técnicos de informações do data set|
| DETAILS | usado para mais deltahes quando usados com DATASETS e LIBS |
| LIBS | informar a biblioteca que desejamos detalhes |
| DATA | refrenciar o datasets que desjamos infomrações |


Nesse primeiro passo realizei toda importanções das bases de dados para o projeto.
![image](https://github.com/user-attachments/assets/37a5e747-e2d4-4abb-aee9-526a42e6c427)

Usando primeiros códigos em SAS

![image](https://github.com/user-attachments/assets/897e5436-4d1a-412a-a4d6-2b8075751635)

Resultados

![image](https://github.com/user-attachments/assets/88367504-ca38-425f-b8bd-29d6b09b38da)

### Checagem das bases

Comando details
![image](https://github.com/user-attachments/assets/00628788-dee3-464c-a8db-e784b062d128)

resultado

![image](https://github.com/user-attachments/assets/6b8b85e4-c5d5-4302-9eeb-49971baf323e)

Obs. Entries or Index = Rows
Vars = columns

### Uma forma de organizar Datas
#### CONTENTS

![image](https://github.com/user-attachments/assets/90aaae38-0bf8-4c78-85a3-d3ef390a66b8)

Resultados
![image](https://github.com/user-attachments/assets/ede2daf9-d8df-4f47-97e5-93eac40b60f4)
![image](https://github.com/user-attachments/assets/116c75c9-be09-4125-ab15-68a9df0979ba)

#### PRINT

Mostra valores espercificos em uma base procuradas
Entrada Código

![image](https://github.com/user-attachments/assets/22332afe-72d8-4c74-9d67-9a9554976dd7)
Sáida resultado
![image](https://github.com/user-attachments/assets/5e82ec88-5b7a-4c1c-bc18-c8240e710586)

Como resultado do PRINT temos a lista da tabela,
>[!note]
>todos valores não tem caracteres especiais

Formatos datas são salvos com valores númericos geralmente são com anos  + meses ou então mes + dia para facilitar comparações.
ex.: 202503 0922


## Visualizando Frequências

| VARIAVEL | DESCRIPTION |
| FREQ | gerar um relatório de frequencias |
| table | informa quais colunas queremos detalhar a frequencias usado com FREQ |
| nlevels | gera uma em nio micro somente com quantidade de count destinct  usado com FREQ e DATA |
| IF | condicionais para fazer novas validações |
| Data | seta uma nova váriaveis |
| SET | informa com base será setada a váriavel |
| THEN | condicional se o if for verdadeiro |
| ELSE | condicional se o if for falso |



O comando PROC FREQ ajuda a organizar frequencias e são muito usados em SAS


### Relatórios de Frequências
Entrada 
![image](https://github.com/user-attachments/assets/342a2be0-23a2-4221-8edc-7ca77cac5acb)

Saídas
![image](https://github.com/user-attachments/assets/8491b676-35e0-4599-a539-8175984d51ee)

NLevels

Detalha a soma de quantidade de valores destitos em uma base
![image](https://github.com/user-attachments/assets/36dbc73b-5006-418a-af68-e37f75d0168e)

resultado

![image](https://github.com/user-attachments/assets/0eba6679-c6b2-49b9-9775-58d12f1b6647)

### Criação de uma nova variável

Quando queremos criar uma váriael como true ou falso ou 0 e 1 para dizer se algo é ou não é ou então existe ou não existe etc.

#### CONDICIONAIS COM IF ELSE THEN DATA E SET

![image](https://github.com/user-attachments/assets/2ccb315a-356b-495b-8584-1f0fe882243a)


Resultado
![image](https://github.com/user-attachments/assets/9a42900c-af78-407b-8fb3-49dd13be5bcf)
![image](https://github.com/user-attachments/assets/94fb0a0b-3949-4ee2-9422-a228bb4873c1)


## Continuando com Frequências
### Frequências cruzadas
### Continuando com Frequências cruzadas
### Em busca de chave única
### Comentários e Salvar a Base

## Trabalhando com problemas na base
### Ausências de informações
### Múltiplos Filtros
### Múltiplos condicionais
### Corrigindo os Missings
### Conectando e salvando a base

## Introdução aos formatos
### Obtendo estado a partir do CEP
### Formato e tamanho
### Subtexto
### Convertendo um texto em número

## Usando formatos personalizados
### Como agilizar processos
### Formatos personalizados
### Usando formatos a nosso favor
### Conectar e salvar
