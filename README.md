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
| PROC   | comando inicial para rodar querys  vers tabelas de PROCS abaixo|
| RUN   | para finalizar a querys |
| DATASETS | para rodar um dataset e mostrar alguns detalhes |
| LIBNAME | para declarar um nome de uma biblioteca e usar seu conteúdo |
| PRINT | retorna todos valores em um dataset como a sua tabela geral |
| CONTENT | mostra detalhes mais técnicos de informações do data set|
| DETAILS | usado para mais deltahes quando usados com DATASETS e LIBS |
| LIBS | informar a biblioteca que desejamos detalhes |
| DATA | refrenciar o datasets que desjamos infomrações |

| TABELA DE PROC'S|
| QUERY | DESCRICAO |
|--------|------------|
| PROC DATASETS | Retorna informações da tabelas com detatlhes|
| PROC FORMAT   | Atribui formatos particulas aos datasets |
| PROC CONTENTS   | Gera uma tabela com informações do data sete |
| PROC PRINT | Printa toda tabela do datasetes |
| DATA | para declarar um nome de uma biblioteca e usar seu conteúdo |



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

NOOBS 
usamos noobs quando queremos sumir a colunas observação
![image](https://github.com/user-attachments/assets/c6a24b5a-6aaf-41e0-9845-fa50558d69b1)


Resultados
![image](https://github.com/user-attachments/assets/ec379700-739f-43d8-b095-da58430ed650)

Como resultado do PRINT temos a lista da tabela,
>[!note]
>todos valores não tem caracteres especiais

Formatos datas são salvos com valores númericos geralmente são com anos  + meses ou então mes + dia para facilitar comparações.
ex.: 202503 0922


## Visualizando Frequências

| VARIAVEL | DESCRIPTION |
|----------|------------|
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

| VARIAVEL | DESCRIPTION |
|----------|------------|
| noobs | remove observações do prints |
| norow | remove row da analise cruzada |
| nofreq | remove freq da analise cruzada |
| nopercent | remove percente analise cruzadas |
| nocol | remove col da analise cruzada |
| rename | renomeia uma coluna |
| label | adiciona metadados as coluans |




### Frequências cruzadas

Usamos * para realizar conferencia cruzadas
![image](https://github.com/user-attachments/assets/952f894c-7206-4f85-bcaf-c3d4280f762b)

resultados
![image](https://github.com/user-attachments/assets/875ea308-11d4-42cf-833e-22e4e7147587)

/ no usamos para remorer algum pronto da observação cruzada

### Continuando com Frequências cruzadas
### Em busca de chave única
Entrada

![image](https://github.com/user-attachments/assets/39a59d45-673d-47c4-828f-337888e81eb6)

Saída
![image](https://github.com/user-attachments/assets/5851de9e-38a5-4669-b4bd-b5bd512feb51)


### Comentários e Salvar a Base

Entradas
![image](https://github.com/user-attachments/assets/8d66de07-e52d-4eb1-b0b7-89a8969d2ae9)

RESULTADOS 
![image](https://github.com/user-attachments/assets/97ae924b-8f22-40ec-a7eb-45d4ae51f4d7)
![image](https://github.com/user-attachments/assets/b21383b6-6e30-4f9d-a34a-dfbcac77a910)

Comentários

![image](https://github.com/user-attachments/assets/d96cab12-49b0-4a78-94f8-e90caf312723)

RESULTADO CÓDIGO PROG 1

```SAS

/** 
		PROGRAMA QUE ANALISA BASE DE PRODUTOS 
**/

/** inicia abrindo a biblioteca e direcionando o caminho **/

LIBNAME Aulas "/home/u64008132/AulasPlay";

/** localiza a tabela e retorna mais informações como detalhes como numero de colunas e também numero de **/
PROC DATASETS
	lib=Aulas details;
RUN;

/** abre uma tabela com metainformações da tabela de origem como metadados **/
PROC CONTENTS
	DATA= Aulas.cadastro_produto;
RUN;

/** printa toda tabela para visualização com todas linhas e colunas para ver os dados**/

PROC PRINT
	DATA = aulas.cadastro_produto noobs;
RUN;

/** gera uma tabela com frequencias de dados como count distints**/
PROC FREQ
	DATA = aulas.cadastro_produto nlevels;
	TABLES genero plataforma nome;
RUN;

/** Gera um novo dataset para eploração de dados usando if e else e then para analises profunda dos dados**/
DATA testes;
set aulas.cadastro_produto;

IF data > 201605
	THEN lancamento = 1;
	ELSE lancamento = 0;
RUN;

/** Faz analise de frequencia para validar a criação de lancamento**/
PROC FREQ 
	DATA = testes;
	table lancamento;
RUN;

/** Graças ao * realiza a análise cruzada **/
PROC FREQ 
	DATA = testes;
	table genero*lancamento
	/nocol nopercent norow;
RUN;

/**-----------------------------------------------------------------------------------------**/
/** Cria metadados para nosso componentes salva o teste no sistema e também renomeia colunas**/
/**-----------------------------------------------------------------------------------------**/
DATA aulas.cadastro_produtos_v2;
set testes;
rename lancamento = flag_lancamentos;
label Genero = "Genero para o tipo de jogo"
	  lancamento = "Recebe 1 se foi lançado ou 0 se não foi lançado antes de '2016'";
RUN;

PROC CONTENTS
	DATA= Aulas.cadastro_produtos_v2;
RUN;


```
## Trabalhando com problemas na base
| VARIAVEL | DESCRIPTION |
|----------|------------|
| WHERE | localizar informações especificas |
| is missing | usado com WHERE para achar valores null |
| WHEN | usado com if e THEN DO |
| THEN DO | Usado com if |
| END | FINALIZA causa |
| FORMAT | define o tamanho do char o numeric |



### Ausências de informações

usamos comando where para validar quando valores são faltantes
o MISSing também pode ser um único .

entradas

![image](https://github.com/user-attachments/assets/8f3b9e52-de12-4527-b44b-0d7d7d9e5885)

saídas

![image](https://github.com/user-attachments/assets/7461ff07-b576-4c72-8c6e-705a60dd7f57)

### Múltiplos Filtros

![image](https://github.com/user-attachments/assets/c901d050-6235-4096-8d58-5316310d7dd6)

saída

![image](https://github.com/user-attachments/assets/af45ef4d-4dd0-489e-af17-e1426b8564e2)

![image](https://github.com/user-attachments/assets/0ed77753-9763-475a-8f30-8a58c18577f2)

![image](https://github.com/user-attachments/assets/1e402175-511e-45df-ac24-8d017e622c34)

![image](https://github.com/user-attachments/assets/6236c2e7-bbce-408b-abba-a2355079dc53)

![image](https://github.com/user-attachments/assets/19048b11-d848-40e8-b40e-27e1bb311dcf)



### Múltiplos condicionais

Multiplos condicionais de busca e substituição.

![image](https://github.com/user-attachments/assets/c441c750-8b53-4f1a-b403-ae7faf289d98)


![image](https://github.com/user-attachments/assets/b5de6cf6-279f-4834-af1c-330ee1702c74)

### Corrigindo os Missings

![image](https://github.com/user-attachments/assets/2cc831b0-d795-4841-ace2-7b045715d90f)

![image](https://github.com/user-attachments/assets/80dae864-d237-4f5b-a4e3-31f42ff96c8b)


Corrigindo os dados com DATA... SET... IF.... THEN DO.. SELECT .... WHEN... END .. END .. RUN

Entrada

![image](https://github.com/user-attachments/assets/a4221fda-50c2-4fd3-b366-3f2ff9fae501)

Saída

![image](https://github.com/user-attachments/assets/9da6b587-fc1b-4604-be27-eb582a803e27)

Confirmando se os dados foram todos corrigidos corretamente.

Entrada

![image](https://github.com/user-attachments/assets/b98be24f-b053-4767-9f7f-9cea5f022546)

Saída

![image](https://github.com/user-attachments/assets/783bc2a3-19f2-4a33-bf31-a0f2728b0e53)

### Conectando e salvando a base

```SAS
/** ANÁLISE DE VAR DATA **/


/** inicia abrindo a biblioteca e direcionando o caminho **/

LIBNAME Aulas "/home/u64008132/AulasPlay";
/** Clausula where ajuda a encontrar valores especificos **/



PROC FREQ
	data = aulas.cadastro_produtos_v2;
	table data;
RUN;

/** 
		PROGRAMA QUE ANALISA BASE DE PRODUTOS 
**/

DATA teste_v1;
set aulas.cadastro_produtos_v2;
WHERE data IS MISSING;
RUN;

DATA teste_v1;
set aulas.cadastro_produtos_v2;
	WHERE nome = "Fireshock"
	OR nome = "Forgotten Echo"
	OR nome = "Soccer";
RUN;

DATA teste_v2;
set aulas.cadastro_produtos_v2;
	WHERE nome in ("Fireshock", "Forgotten Echo", "Soccer");
RUN;

/* -------------------------------------------------------------  */
/* Busca somente arquivos onde datas estão null ou missing 0 ou . */
/* -------------------------------------------------------------   */
PROC FREQ DATA=teste_v2;
    TABLES nome*data / LIST MISSING;
RUN;		

/* 
	verificando valores de nome onde será verificado valores missing. 
*/
PROC FREQ
	DATA = teste_v1
	(WHERE=(nome in ("Fireshock", "Forgotten Echo", "Soccer")));

RUN;

* testando busca com datas e substituição;
DATA teste_v3;
set aulas.cadastro_produtos_v2;
IF DATA = . THEN DO;
	SELECT(nome);
		WHEN ("Fireshock") 		data= 201706;
		WHEN ("Forgotten Echo") data=201411;
		WHEN ("Soccer") 		data = 201709;
	END;
END;
RUN;

/* ------------------------------------------------------ */
/* CONFIRMANDO SE DADOS FORAM CORRIGIDOS */
/* ------------------------------------------------------ */

PROC FREQ
	DATA = teste_v3
		(WHERE=(nome in ("Fireshock", "Forgotten Echo", "Soccer")));
	table nome*data;
RUN;


DATA aulas.cadastro_produtos_v3;
set testes_v3;
rename lancamento = flag_lancamentos;
label Genero = "Genero para o tipo de jogo"
	  lancamento = "Recebe 1 se foi lançado ou 0 se não foi lançado antes de '2016'";
RUN;

PROC CONTENTS
	DATA = aulas.cadastro_produtos_v3;
RUN;

PROC PRINT
	DATA = aulas.cadastro_produtos_v3 noobs;
RUN;


PROC PRINT
	DATA = aulas.cadastro_produto noobs;
RUN;

```

## Introdução aos formatos

| VARIAVEL | DESCRIPTION |
|----------|------------|
| FORMAT | define o tamanho do char o numeric |
| LENGHT | Usado para formar váriaveis numericas|
|substr | função que pega valores e quebra o txt, arg 1 é a colunas arg2 é inicio e arg3 final|




### Obtendo estado a partir do CEP

![image](https://github.com/user-attachments/assets/07f19e5a-16a0-4100-812b-d07de612ac5a)

![image](https://github.com/user-attachments/assets/462a8a16-e9ea-494d-8b43-ad67dec818be)

### Formato e tamanho

Usamos FORMAT para converter valores antes de modificar

![image](https://github.com/user-attachments/assets/e896c79f-fd7b-466f-9eeb-360e748cc6c8)

SAÍDA

![image](https://github.com/user-attachments/assets/0f2b9601-96cf-4c56-99be-61ad9e8660fe)


### Subtexto

Para gerar uma substring podemos usar a váriavel substr que quebra strings em uma local especifico.

Entrada

![image](https://github.com/user-attachments/assets/32c4b8e5-4ff3-40d4-83a4-c4a517323737)

Saída

![image](https://github.com/user-attachments/assets/f3fce7b6-6ede-4cd3-af71-12ca86575382)

### Convertendo um texto em número

Podemos converter para númerico usando *1 para calcular em valore númericos
mas essa conversão é implicita e retira nosso controle de conersão

Entrada

![image](https://github.com/user-attachments/assets/83bc3cc0-9587-4772-ba23-36021a7ad2f2)

saída
![image](https://github.com/user-attachments/assets/125f48a5-7b49-414e-a1d5-8d0aa90d2892)

Meio mais eficaz é usar input para transformar em númeric, input recebe o valores da colunas, e o formant pode ser numero mais ponto ou então best mais ponto como no print

Entrada

![image](https://github.com/user-attachments/assets/39018ca0-3839-4082-8463-56b260c6cb80)
![image](https://github.com/user-attachments/assets/d5c31e96-4b88-4280-b8a4-28d7444d4265)

Saída

![image](https://github.com/user-attachments/assets/90bf5e71-1594-421f-9a74-1b8c6a648416)

## Usando formatos personalizados

| VARIAVEL | DESCRIPTION |
|----------|------------|
| DROP | remove colunas informadas da tabela |
| KEEP | Mantem somente as colunas informadas|
| OPTIONS | Seta váriaveis globais |
| obs | seta quantidade de dadaos retornados em uma pesquisa MAX informa o total de linhas de um df|
|MAX | parametro para váriavel obs que informa o maximo de linhas que um dataframe tem que receber|
| LOW | informa o menor valores possivel em format com values |
| hight | informa o maior valores possivel em format com values |
| <-< | informa que valore estão entre meno que etc |


### Como agilizar processos

O comanda DROP remove váriaveis e columns desnecessários no projeto

Entrada
![image](https://github.com/user-attachments/assets/70c2a9fb-ab5a-4271-b37b-aeb228dc7d90)


sáida

![image](https://github.com/user-attachments/assets/f85ab9a3-d339-40ae-8992-42007fc955e3)

O comando Keep mantem somente as columns necessárias para o projeto.

Entrada

![image](https://github.com/user-attachments/assets/51edb4ea-2a15-4586-92d3-06f4807e7aed)


Saída

![image](https://github.com/user-attachments/assets/3a49cfe8-50ef-41c2-8f8e-c64c28fb105a)


usando OBS para informar quantidade de dados de retorno que queremos em uma base

![image](https://github.com/user-attachments/assets/1ed57486-5b50-4175-b8ab-b94735ea8140)

![image](https://github.com/user-attachments/assets/4ccfdd38-32bd-4426-9d1e-edf22bc79b80)

Podemos setar váriaveis globais com OPTION
![image](https://github.com/user-attachments/assets/a67948db-f96b-4063-8b3a-7c544de3f3e5)


### Formatos personalizados

Possivel usar PROC FORMAT para criar formatos personalizados.

![image](https://github.com/user-attachments/assets/f95f2501-e31c-4cc2-a151-cbc46f41d315)
![image](https://github.com/user-attachments/assets/18b06724-ec72-4bc4-a99d-f0fd4ba16242)

![image](https://github.com/user-attachments/assets/b956f4f7-f446-42f7-a358-6416b9a224b6)

### Usando formatos a nosso favor

Podemos usar Low para informar que é o menor valor possivel e HIGH para inaforma o maior valor possivel

![image](https://github.com/user-attachments/assets/309488aa-9378-488d-bf53-cc4bcff2b7f9)

Transformando dados para TEXTO em númericos conforme regras

![image](https://github.com/user-attachments/assets/9c792a53-a956-4b42-85f9-22194125f600)
![image](https://github.com/user-attachments/assets/8d2384dc-f791-400f-b6d2-06bfe7635686)

ENTRADA

![image](https://github.com/user-attachments/assets/175b51c5-7c33-440a-b1b5-509045b7ef81)


SAÍDA 
![image](https://github.com/user-attachments/assets/e56b304c-4989-4188-b154-8b52444b061f)
![image](https://github.com/user-attachments/assets/9b08e4ff-a78c-4291-91a3-e4e666b2a95e)


### Conectar e salvar

```SAS

/** inicia abrindo a biblioteca e direcionando o caminho **/

LIBNAME Aulas "/home/u64008132/AulasPlay";

OPTIONS obs=15;

DATA teste_4;
set aulas.cadastro_cliente;

drop nome, nascimento, sexo;

RUN;

DATA teste_4;
set aulas.cadastro_cliente (obs=15 keep=cpf cep);

precep = input(substr(cep, 1, 2), best.);

RUN;

PROC PRINT
	DATA= teste_4;
RUN;


PROC FORMAT;
	VALUE estadosnun_
		LOW-09 		= 'GRANDE SAO PAULO'
		10-19 		= "INTERIOR DE SP"
		19 <-< 29	= "RIO DE JANEIRO"
		30-39		= "MINAS GERAIS"
		80-87 		= "PARANA"
		OTHER 		= "UNKNON - DEMAIS";
RUN;


DATA teste_v5;
set aulas.cadastro_cliente;

estados = put(input(substr(cep, 1,2), best.), estados_.);

RUN;


PROC FREQ
	DATA =teste_v5;
	table estados;
RUN;



PROC FORMAT;
	INVALUE estadosnun_
		"01"-"09" 	= 1
		"10"-"19" 	= 2
		"20"-"28"	= 3
		"30"-"39"	= 4
		"80"-"87"	= 5
		OTHER 		= 6;
	VALUE estadostxt_
		1 		= 'GRANDE SAO PAULO'
		2 		= "INTERIOR DE SP"
		3		= "RIO DE JANEIRO"
		4		= "MINAS GERAIS"
		5 		= "PARANA"
		OTHER	= "UNKNON - DEMAIS"; 
RUN;


DATA teste_v5;
set aulas.cadastro_cliente;

estados = input(substr(cep, 1,2), estadosnun_.);
FORMAT estados estadostxt_.;

RUN;
	
```
