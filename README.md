# TRABALHO 01:  Título do Trabalho
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>
Integrantes do grupo<br>
primeiro_componente_do_grupo:email_primeiro_componente@dominio.com<br>
segundo_componente_do_grupo:email_segundo_componente@dominio.com<br>
...<br>

### 2.INTRODUÇÃO E MOTIVAÇÃO<br>
Este documento contém a especificação do projeto do banco de dados <nome do projeto> 
<br>e motivação da escolha realizada. <br>

> A empresa "Devcom Projetos" visa colaborar com desenvolvimento de projetos para uma sociedade melhor. Sabendo-se dos desafios para gerenciar projetos dentro de uma empresa e visando unir as informações relativas a funcionários, departamentos e projetos em um mesmo local, ficamos motivados com o desenvolvimento deste sistema. O Sistema "Devcom" tem como objetivo gerenciar todas as informações ao desenvolvimento das atividades de projetos em diversas localidades do país. Para realizar suas operações adequadamente e empresa necessita que sistema que armazene informações relativas aos Projetos, Departamentos e Empregados, além de também armazenar dados sobre  Dependentes e Históricos de Salário dos empregados. O sistema deverá gerar um conjunto de relatórios que por sua vez atenderá os anseios da empresa em questão.
 

### 3.MINI-MUNDO<br>

Descrever o mini-mundo! (Não deve ser maior do que 30 linhas, se necessário resumir para justar) <br>
Entrevista com o usuário e identificação dos requisitos.(quando for o caso de sistemas com cliente  real)<br>
Descrição textual das regras de negócio definidas como um  subconjunto do mundo real 
cujos elementos são propriedades que desejamos incluir, processar, armazenar, 
gerenciar, atualizar, e que descrevem a proposta/solução a ser desenvolvida.

> O sistema proposto para a "Devcom Projetos conterá as informacões aqui detalhadas. Dos Projetos serão armazenados o número, nome e cidade. Dos Departamentos serão armazenados o número e nome. O cliente destacou que cada projeto pode ter vários departamentos auxiliando no seu desenvolvimento, e cada departamento pode estar envolvido em vários projetos. Os dados relativos aos empregados que serão armazenados são: rg, nome, cpf, salário, data inicial do salario e supervisor de cada empregado. É importante destacar que cada empregado pode ser supervisionado por outro empregado, e obrigatoriamente deve estar alocado a um único departamento, mas pode gerenciar vários departamentos ou não gerenciar nenhum. Um empregado também pode participar de vários projetos, caso seja necessário, mas não precisa obrigatoriamente estar alocado em algum projeto. Com relação aos dependentes serão armazenadas as informações de nome do dependente, data de nascimento, sexo e grau de parentesco. Cada empregado pode ter vários dependentes, mas um dependente esta associado apenas a um único empregado. Com relação ao histórico de salário devemos armazenar as informações de valor do salário, data de início do salário no período e data final do salário no período. É importante lembrar que cada funcionario pode ter diversos eventos de histórico de salário associados a ele visto que este dado pode ser alterado várias vezes. 

### 4.PROTOTIPAÇÃO, PERGUNTAS A SEREM RESPONDIDAS E TABELA DE DADOS<br>
#### 4.1 RASCUNHOS BÁSICOS DA INTERFACE (MOCKUPS)<br>
Neste ponto a codificação não e necessária, somente as ideias de telas devem ser criadas, o princípio aqui é pensar na criação da interface para identificar possíveis informações a serem armazenadas ou descartadas <br>

Sugestão: https://balsamiq.com/products/mockups/<br>

![Alt text](https://github.com/discipbd1/trab01/blob/master/balsamiq.png?raw=true "Title")
![Arquivo PDF do Protótipo Balsamiq feito para Empresa Devcom](https://github.com/discipbd1/trab01/blob/master/arquivos/EmpresaDevcom.pdf?raw=true "Empresa Devcom")
#### 4.2 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes? 
    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!
    
> A Empresa DevCom precisa inicialmente dos seguintes relatórios:
* Relatório que mostre o nome de cada supervisor(a) e a quantidade de empregados supervisionados.
* Relatório relativo aos os supervisores e supervisionados. O resultado deve conter o nome do supervisor e nome do supervisionado além da quantidade total de horas que cada supervisionado tem alocada aos projetos existentes na empresa.
* Relatorio que mostre para cada linha obtida o nome do departamento, o valor individual de cada salario existente no  departamento e a média geral de salarios dentre todos os empregados. Os resultados devem ser apresentados ordenados por departamento.
* Relatório que mostre as informações relacionadas a todos empregados de empresa (sem excluir ninguém). As linhas resultantes devem conter informações sobre: rg, nome, salario do empregado, data de início do salario atual, nomes dos projetos que participa, quantidade de horas e localização nos referidos projetos, numero e nome dos departamentos aos quais está alocado, informações do historico de salário como inicio, fim, e valores de salarios antigos que foram inclusos na referida tabela (caso possuam informações na mesma), além de todas informações relativas aos dependentes. 
>> ##### Observações: <br> a) perceba que este relatório pode conter linhas com alguns dados repetidos (mas não todos). <br>  b) para os empregados que não possuirem alguma destas informações o valor no registro deve aparecer sem informação/nulo. 
* Relatório que obtenha a frequencia absoluta e frequencia relativa da quantidade de cpfs únicos no relatório anterior. Apresente os resultados ordenados de forma decrescente pela frequencia relativa.

1- Relatório que mostra todas as pessoas de cada bairro vacinadas.
2- Relatório que mostra a quantidade de pessoas completamente imunizadas na cidade.
3- Relatório que mostra todas como estão avançando as vacinações por faixa etária.
4- Relatório que mostra qual vacina mais está sendo utilizda.
5- Relatório que mostra qual o local onde as pessoas mais estão sendo vacinadas.
 
 
#### 4.3 TABELA DE DADOS DO SISTEMA:
    a) Esta tabela deve conter todos os atributos do sistema e um mínimo de 10 linhas/registros de dados.
    b) Esta tabela tem a intenção de simular um relatório com todos os dados que serão armazenados 
    
![Exemplo de Tabela de dados da Empresa Devcom](https://github.com/discipbd1/trab01/blob/master/arquivos/TabelaEmpresaDevCom_sample.xlsx?raw=true "Tabela - Empresa Devcom")
    
    
### 5.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)       
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   
        
![Alt text](https://github.com/discipbd1/trab01/blob/master/images/concept_sample.png?raw=true "Modelo Conceitual")
    
    
        
    
#### 5.1 Validação do Modelo Conceitual
    [Grupo01]: [Nomes dos que participaram na avaliação]
    [Grupo02]: [Nomes dos que participaram na avaliação]

#### 5.2 Descrição dos dados 
    [objeto]: [descrição do objeto]
    
    PESSOA: Tabela que armazena as informações do vacinado
    CPF: campo que armazena o número de Cadastro de Pessoa Física de cada vacinado
    NOME: campo que armazena o nome do vacinado
    DATA_NASC: campo que armazena a data de nascimento do vacinado
    DESCRICAO_LOGRADOURO: campo que armazena nome do logradouro do vacinado
    NUMERO_LOGRADOROU: campo que armazena numero da residencia do vacinado
    BAIRRO: campo que armazena o bairro do vacinado
    CEP: campo que armazena o cep do vacinado
    ENFERMEIRA: Tabela que armazena as informações da enfermeira
    COFEN: campo que armazena o cofen da enfermeira
    NOME: campo que armazena o nome da enfermeira
    VACINA: Tabela que armazenas as informações da vacina
    COD_VACINA: campo que armazena o código de uma determinada vacina no sistema
    DESCRICAO:  campo que armazena o nome da vacina
    LOCALIDADE: Tabela que armazena as informações dos locais de aplicação das vacinas
    ID_LOCAL: campo que armazena o codigo de um local de vacinação
    DESCRICAO: campo que armazena a descrição do local
    VACINACAO: Tabela que armazena dados de uma vacina aplicada
    ID_APLICACAO: campo que armazena o codigo no sistema de uma vacina aplicada
    DATA_DOSE: campo que armazena a data da aplicação
    NUM_DOSE: campo que armazena o numero da dose que foi aplicada
    fk_PESSOA_cpf: campo que armazena o CPF da pessoa vacinada
    fk_VACINA_cod: campo que armazena o codigo da vacina aplicada
    fk_ENFERMEIRA_cofen: campo que armazena o codigo da enfermeira que aplicou a vacina
    fk_LOCALIDADE_id_localidade: campo que armazena o codigo da localidade onde foi aplicada a vacina
    CONTATO: Tabela que armazena informações de contato de uma pessoa
    ID_CONTATO: campo que armazena o codigo no sistema referente a um numero de telefone de uma pessoa
    TIPO: campo que armazena o tipo de contato que se refere o registro
    DESCRICAO: campo que armazena um numero contato de uma pessoa
    fk_PESSOA_cpf: campo que armazena o CPF da pessoa dona do telefone de contato



### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual 
        (não serão aceitos modelos que não estejam em conformidade)

### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL 
        (criação de tabelas, alterações, etc..) 
    create table PESSOA(
    cpf int PRIMARY KEY,
    nome varchar(50),
    data_nasc date,
    descricao_logradouro varchar(50),
    numero_logradouro int,
    bairro varchar(50),
    cep int
    );

    create table ENFERMEIRA(
        cofen int PRIMARY KEY,
        nome varchar(50)
    );

    create table VACINA(
        cod_vacina int PRIMARY KEY,
        descricao varchar(50)
    );

    create table LOCALIDADE(
        id_local int PRIMARY KEY,
        descricao varchar(50)
    );

    create table VACINACAO(
        id_aplicacao int PRIMARY KEY,
        data_dose date,
        num_dose int,
        fk_PESSOA_cpf int,
        fk_VACINA_cod_vac int,
        fk_ENFERMEIRA_cofen int,
        fk_LOCALIDADE_id_localidade int,

        FOREIGN KEY(fk_PESSOA_cpf) REFERENCES PESSOA(cpf),
        FOREIGN KEY(fk_VACINA_cod_vac) REFERENCES VACINA(cod_vacina),
        FOREIGN KEY(fk_ENFERMEIRA_cofen) REFERENCES ENFERMEIRA(cofen),
        FOREIGN KEY(fk_LOCALIDADE_id_localidade) REFERENCES LOCALIDADE(id_local)

    );
    create table CONTATO(
        id_contato int PRIMARY KEY,
        tipo varchar(30),
        descricao integer,
        fk_PESSOA_cpf,
        FOREIGN KEY(fk_PESSOA_cpf) REFERENCES PESSOA(cpf)
    );

       
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) inclusão das instruções de inserção dos dados nas tabelas criadas pelo script de modelo físico
        (Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        b) Criar um novo banco de dados para testar a restauracao 
        (em caso de falha na restauração o grupo não pontuará neste quesito)
        c) formato .SQL
        insert into CONTATO (id_contato,tipo,descricao,fk_PESSOA_cpf) values 
        ('1','celular','998677631','111'),
        ('2','celular','998477631','222'),
        ('3','celular','998577631','333'),
        ('4','celular','998977631','444'),
        ('5','celular','998177631','555'),
        ('6','fixo','30604020','111'),
        ('7','fixo','30614020','222'),
        ('8','fixo','30624020','333'),
        ('9','fixo','30634020','444'),
        ('10','fixo','30644020','555');
        insert into VACINACAO (data_dose,num_dose,id_aplicacao,fk_PESSOA_cpf,fk_VACINA_cod_vac,fk_ENFERMEIRA_cofen,fk_LOCALIDADE_id_LOCALIDADE) values ('2021-07-16','1','3','333','1','123','3');
        insert into VACINACAO (data_dose,num_dose,id_aplicacao,fk_PESSOA_cpf,fk_VACINA_cod_vac,fk_ENFERMEIRA_cofen,fk_LOCALIDADE_id_LOCALIDADE) values ('2021-07-16','1','4','444','2','333','4');
        insert into VACINACAO (data_dose,num_dose,id_aplicacao,fk_PESSOA_cpf,fk_VACINA_cod_vac,fk_ENFERMEIRA_cofen,fk_LOCALIDADE_id_LOCALIDADE) values ('2021-07-16','1','5','555','3','333','5');
        insert into VACINACAO (data_dose,num_dose,id_aplicacao,fk_PESSOA_cpf,fk_VACINA_cod_vac,fk_ENFERMEIRA_cofen,fk_LOCALIDADE_id_LOCALIDADE) values ('2021-07-16','1','6','666','5','666','6');
        insert into VACINACAO (data_dose,num_dose,id_aplicacao,fk_PESSOA_cpf,fk_VACINA_cod_vac,fk_ENFERMEIRA_cofen,fk_LOCALIDADE_id_LOCALIDADE) values ('2021-07-15','1','7','101','1','333','2');
        insert into VACINACAO (data_dose,num_dose,id_aplicacao,fk_PESSOA_cpf,fk_VACINA_cod_vac,fk_ENFERMEIRA_cofen,fk_LOCALIDADE_id_LOCALIDADE) values ('2021-07-16','1','8','999','5','444','5');
        insert into VACINACAO (data_dose,num_dose,id_aplicacao,fk_PESSOA_cpf,fk_VACINA_cod_vac,fk_ENFERMEIRA_cofen,fk_LOCALIDADE_id_LOCALIDADE) values ('2021-07-16','1','9','888','3','666','7');
        insert into VACINACAO (data_dose,num_dose,id_aplicacao,fk_PESSOA_cpf,fk_VACINA_cod_vac,fk_ENFERMEIRA_cofen,fk_LOCALIDADE_id_LOCALIDADE) values ('2021-07-16','1','10','777','1','555','9');
        insert into LOCALIDADE (id_local,descricao) values ('3','UBS Campinho da Serra');
        insert into LOCALIDADE (id_local,descricao) values ('4','UBS Carapebus');
        insert into LOCALIDADE (id_local,descricao) values ('5','UBS Campinho da Serra');
        insert into LOCALIDADE (id_local,descricao) values ('6','UBS Manoel Plaza');
        insert into LOCALIDADE (id_local,descricao) values ('7','UBS Manguinhos');
        insert into LOCALIDADE (id_local,descricao) values ('8','Sao Marcos');
        insert into LOCALIDADE (id_local,descricao) values ('9','UBS Oceania');
        insert into VACINA (cod_vacina,descricao) values ('3','Pfizer');
        insert into VACINA (cod_vacina,descricao) values ('4','Moderna');
        insert into VACINA (cod_vacina,descricao) values ('5','Sputnik V');
        insert into VACINA (cod_vacina,descricao) values ('6','Covishield');
        insert into VACINA (cod_vacina,descricao) values ('7','Janssen');
        insert into VACINA (cod_vacina,descricao) values ('8','Cansino');
        insert into VACINA (cod_vacina,descricao) values ('9','Covaxin');
        insert into VACINA (cod_vacina,descricao) values ('10','kovivac');
        insert into ENFERMEIRA(cofen, nome) values ('333','Carlos André');
        insert into ENFERMEIRA(cofen, nome) values ('444','Adriana Lima');
        insert into ENFERMEIRA(cofen, nome) values ('555','Brenda Costa');
        insert into ENFERMEIRA(cofen, nome) values ('666','Douglas Henrique');
        insert into ENFERMEIRA(cofen, nome) values ('777','Izabella Campos');
        insert into ENFERMEIRA(cofen, nome) values ('888','Tiago Pessoa');
        insert into ENFERMEIRA(cofen, nome) values ('999','Geovana Pires');
        insert into ENFERMEIRA(cofen, nome) values ('101','Geovane Ceolim');
        insert into PESSOA (cpf,nome,data_nasc,descricao_logradouro,bairro,numero_logradouro,cep) values ('333','Miria Gomes','1981-02-16','Rua dos ipes','Santa luzia','301','29165757');
        insert into PESSOA (cpf,nome,data_nasc,descricao_logradouro,bairro,numero_logradouro,cep) values ('444','Jonias de Paula','1956-11-01','Rua dos ipes','Santa luzia','301','29165757');
        insert into PESSOA (cpf,nome,data_nasc,descricao_logradouro,bairro,numero_logradouro,cep) values ('555','Paulo Victor','1999-08-27','Rua dos ipes','Santa luzia','301','29165757');
        insert into PESSOA (cpf,nome,data_nasc,descricao_logradouro,bairro,numero_logradouro,cep) values ('666','Izabella Campos','2000-05-25','Assembléia Estadual','Carapebus','256','12345678');
        insert into PESSOA (cpf,nome,data_nasc,descricao_logradouro,bairro,numero_logradouro,cep) values ('777','Ana Clara Campos','2005-01-25','Assembléia Estadual','Carapebus','256','12345678');
        insert into PESSOA (cpf,nome,data_nasc,descricao_logradouro,bairro,numero_logradouro,cep) values ('888','Elizangela Campos','1976-09-24','Assembléia Estadual','Carapebus','256','12345678');
        insert into PESSOA (cpf,nome,data_nasc,descricao_logradouro,bairro,numero_logradouro,cep) values ('999','Jair Trarbach','1945-07-24','Assembléia Estadual','Carapebus','256','12345678');
        insert into PESSOA (cpf,nome,data_nasc,descricao_logradouro,bairro,numero_logradouro,cep) values ('101','George Matheus','1994-08-19','Rua Rio Grande do Sul','José de Anchieta','334','12345678');


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Incluir para cada tópico as instruções SQL + imagens (print da tela) mostrando os resultados.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>
    Select * from CONTATO
    Select * from VACINA
    Select * from LOCALIDADE
    Select * from ENFERMEIRA 
    Select * from PESSOA
    Select * from VACINACAO
># Marco de Entrega 01: Do item 1 até o item 9.1<br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>
#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 02: Do item 9.2 até o ítem 9.10<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 03: Itens 10 e 11<br>
<br>
<br>
<br> 



### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
    
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/
#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


