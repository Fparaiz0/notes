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
