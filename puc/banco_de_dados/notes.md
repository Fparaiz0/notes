# SEMANA 1

### PROPRIEDADES ACID
Para garantir que as transações em um banco de dados sejam confiáveis, especialmente nos bancos de dados relacionais, os SGBDs (sistemas gerais de banco de dados) seguem um conjunto de quatro propriedades sagradas, conhecidas pela sigla ACID:
 - Atomicidade: garante que todos os passos de uma operação (transação) sejam concluídos com sucesso. Se um único passo falhar, toda a operação é desfeita (rollback);
 - Consistência: garante que a transação só levará o banco de dados de um estado válido para outro estado válido, respeitando todas as regras de negócio (ex: saldo não pode ser negativo), como quando eu defino qual tipo de dado uma coluna pode receber, mas a consistência é algo muito mais amplo que somente isto;
 - Isolamento: garante que transações concorrentes (acontecendo ao mesmo tempo) não interfiram umas nas outras. Cada uma "pensa" que está rodando sozinha no sistema;
 - Durabilidade: garante que, uma vez que uma transação é concluída com sucesso (commit), seus resultados são permanentes e não serão perdidos, mesmo em caso de falha do sistema, a menos que seja excluído propositalmente pelo usuário.

### DIFERENÇAS DO SQL PARA O NOSQL
 - SQL: é uma linguagem de programação utilizada para leitura e gerenciamento de dados de um respectivo banco de dados e é relacional, ou seja, é constituído de tabelas e colunas que podem relacionar-se (ex.: chave estrangeira) entre si (daí o nome). Exemplos de implementações de SQL: MySql, Microsoft SQL Server, PostgreSQL e MariaDB;
 - NoSQL: refere-se a uma categoria de bancos de dados não relacionais projetados para armazenar e gerenciar dados flexíveis ou não estruturados.

<hr>

# SEMANA 2

### PENSANDO ANTES DE AGIR
Antes da criação do banco de dados físico é necessário seguir alguns passos a fim de analizar a situação e validar se realmente é preciso o uso do mesmo. Os passos são basicamente:
 - Identificar o problema: por que foi requerida a criação de um banco de dados? Isso pode ser resolvido somente anotando em um bloco de notas ou numa planilha do excel?
 - Modelagem conceitual: aqui começa como se fosse criarmos a "planta" do banco de dados, é onde colhemos as informações do que gostaríamos de armazenar nas respectivas tabelas do banco de dados; possui entidades (cada item da tabela), atributos (características dos atributos) e relacionamentos (tipos de ligações que cada tabela do banco possui entre si);
 - Modelagem lógica: é onde criamos de fato a "planta" do banco, geralmente em softwares como o brModelo ou o Workbench, criamos de forma física o conceito das tabelas, dos relacionamentos entre si e de suas entidades com seus atributos;
 - Modelagem física: é quando já criamos o banco de dados fisicamente, utilizamos queries e podemos realizar qualquer ato do CRUD com o bd.  
