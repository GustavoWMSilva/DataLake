Avaliação Prática em Grupo TG
Vencimento:  quarta, 6 Dez 2023, 23:59
Este trabalho deverá ser realizado em grupos e consiste na criação de um data lake em ambiente de computação na
nuvem. Ele deverá ser alimentado a partir da extração e carga de dados de pelo menos duas fontes de dados.
Enunciado
Cada grupo deverá:
1. Entrar em sua conta de estudante na Microsoft Azure. É possível desenvolver o trabalho na conta de um dos
componentes do grupo. O titular da conta precisará incluir os demais componentes como co-administrador. Para isso,
deve ser utilizado o IAM:
Site está em modo de somente leitura
×
ATENÇÃO:
Todos os recursos criados na Azure durante a execução do trabalho devem ser incluídos em um "Grupo de Recursos"
com o nome grupoNN, sendo que NN corresponde ao número do grupo no Moodle. Para aqueles grupos que já tiverem
criado seu "Grupo de Recursos" anteriormente, esse nome deve ser informado no relatório final (documento PDF).
Além disso, o grupo deve incluir o usuário 10044981@pucrs.br como co-administrador da assinatura "Azure para
Estudantes".
2. Disponibilizar pelo menos duas fontes de dados para alimentação de um data lake.
As duas fontes de dados devem ser relacionadas, ou seja, possuírem um ou mais atributos em comum, de forma a
permitir algum tipo de "cruzamento de dados" entre elas.
Os seguintes sites disponibilizam fontes de dados abertos que podem ser utilizadas, mas os grupos estão livres para
utilizarem outras:
https://dados.gov.br
https://dados.rs.gov.br
https://www.ibge.gov.br
http://www.atlasbrasil.org.br
https://data.world
https://data.worldbank.org
Cada fonte de dados deve ser composta, em seu esquema conceitual, por pelo menos quatro classes, e cada classe
deve possuir alguns milhares de instâncias.
Os sites de onde as fontes de dados foram extraídas devem ser referenciados na documentação.
3. A primeira fonte de dados deve ser disponibilizada sob a forma de um banco de dados relacional empregando o
serviço "Banco de Dados do Azure para servidores flexíveis do PostgreSQL".
Deve ser elaborado script SQL-DDL para criação das tabelas, que devem possuir as necessárias restrições de
integridade, como chaves primárias, chaves estrangeiras e outras.
Deve ser elaborado script SQL-DML para inserção de dados nas tabelas.
4. Além do banco de dados relacional, deve ser disponibilizada uma segunda fonte de dados, relacionada à primeira, que
deve ser uma fonte de dados não relacional. A segunda fonte de dados pode ser disponibilizada em uma das seguintes
formas:
Instância do SGBD MongoDB criada no serviço "Azure Cosmos DB for MongoDB"
Instância do SGBD Cassandra criada no serviço "Azure Managed Instance for Apache Cassandra".
Arquivos armazenados no serviço "Azure NetApp Files".
5. As duas fontes de dados devem ser estruturadas como um Data Lake utilizando o serviço "Azure Synapse Analytics".
1. Deve ser criada uma conta de armazenamento no Azure, a qual será utilizada para armazenar os dados do Data
Lake como BLOBs (Binary Long OBjects):
A essa altura, o grupo de recursos deve estar mais ou menos assim:
2. Agora é necessário criar um Workspace do Synapse Analytics:
A essa altura, o grupo de recursos deve estar mais ou menos assim:
Agora é necessário abrir o Workspace que foi criado:
3. No Workspace, deve-se criar os pipelines de ingestão de dados no Data Lake:
1. Do PostgreSQL:
2. Do MongoDB:
4. Para permitir a realização de consultas SQL sobre os dados carregados, deve ser criado um Banco de Dados SQL:
5. Devem ser criadas pelo menos 3 consultas SQL sobre os dados: uma sobre cada conjunto de dados e uma
terceira com a junção (join) dos dois conjuntos de dados, conforme os exemplos abaixo:
Material a Entregar
Relatório final em formato PDF contendo:
1. Nome do Grupo de Recursos na Microsoft Azure (no padrão grupoNN).
2. Esquema conceitual das duas fontes de dados (Diagrama de Classes criado no Astah).
3. Sobre a primeira fonte de dados:
Esquema lógico de dados do banco de dados PostgreSQL (Diagrama "ER" criado no Astah);
Script SQL-DDL para criação das tabelas; e
Script SQL-DML para inserção de dados (primeiras 10 linhas inseridas).
5. Sobre a segunda fonte de dados:
Esquema lógico não relacional de dados (Diagrama de Classes criado no Astah).
6. Sobre a ingestão de dados:
Imagens capturadas dos pipelines criados.
7. Sobre as consultas ao Data Lake:
Comandos SQL executados e primeiras 10 linhas do resultado.
Critérios de Avaliação
1. Atendimento aos requisitos do enunciado, às boas práticas vistas em aula, criatividade e coerência da aplicaçãoe correção da implementação.

