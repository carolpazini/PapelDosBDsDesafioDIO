# O Papel dos Bancos de Dados SQL e NoSQL na Engenharia de Dados

#### O que é um banco de dados relacional? 
É um banco de dados onde se armazena informações entre si. O esquema de dados é rígido, sabendo-se o que vai ser armazenado no banco. Os dados precisam ser consistentes.

#### O que é um banco de dados não relacional? 
É uma alternativa aos bancos relacionais. Armazena informações não estruturadas e com estruturas diferentes.

#### Bancos NoSQL não foram criados para substituir os bancos SQL, mas sim para complementar. 
Eles foram criados para atender demandas que os bancos SQL não conseguiam atender.

#### Como fazer uma consulta NoSQL? 
Na verdade, os dados ainda precisam ser modelados, e é necessário saber o que se procura para se obter uma resposta. No MongoDB, por exemplo, ainda é possível criar índices.



# Tipos de Bancos de Dados NoSQL


#### Documento
Key-Valor (chave valor)
Orientado a coluna
Orientado a Grafos

#### Grafos
ex.: Neo4j
Os “nós” dos grafos são os dados.
O Neo4j, através uma linguagem, cria relacionamentos em grafos:

Tanto Nós quanto Relacionamentos podem ter propriedades.


#### Coluna/Família de colunas


Ex.: Cassandra
Funciona com registro de transações
linguagem parecia com os dos Bancos sql


#### Chave-Valor

armazena um conjunto de dados, os quais possuem valores exclusivos
Ex.: Redis
https://try.redis.io/

#### Documento

Dados autocontidos e autodescritivos. Permite inconsistência e redundância
ex.: MongoDB
Código aberto
Alta performance
Schema Free
Usa o Json
Suporta Indice
Escala horizontal
Map-reduce
Um dados não pode depender de outro dado
Document ⇒Tupla
Collection ⇒Tabela
Embedding/linking ⇒ join
Usar como grande volumes de dados
dados desestruturados
armazena seus dados utilizando o bson, e não o json.


#### Schema Design

Embedding X Referência
Documentos autocontidos
Documentos com dependência de outros documentos ou collections
Embedding: consulta as informações em uma só query, atualiza o registro em uma operação
Referência: documentos pequenos, não duplica informações, usado quando os dados não são acessados em todas as consultas

###### Relacionamentos:
one-to-one: preferência a atributos chave-valor
one-to-few: preferência ao embedding
one-to-many e many-to-many: preferência a Referência

###### Boas práticas
Evitar documentos grades
usar nomes campos objetivos e curtos
Analisar as queries utilizando o explain()
Atualizar apenas os campos alterados
Evitar negações em queries

Bson: É uma serialização codificada em binário de documentos semelhantes ao Json; Contém extensões que permitem a representação de tipos de dados que não fazem parte da especificação Json

—-----


###### Qual comando utilizado para criar um database no MondoDB?
use <nome_database>

###### O MongoDB suporta restrições de chave estrangeira?
Não

###### Qual o(s) método(s) que podemos utilizar para criar um novo documento?

db.collection.insertOne() ...insertMany() ...insert()

###### Quais as linguagens de consulta utilizadas pelo Neo4j e Cassandra respectivamente?
Cypher e CQL

###### Qual tipo de escalabilidade adiciona mais recurso na máquina?
Vertical

###### Quais tipos de dados podem ser armazenados no Redis?
A maioria dos tipos de dados

###### MongoDB tem suporte a índices?
Sim e seu funcionamento é igual ao dos BD relacionais

###### Qual o(s) método(s) que podemos utilizar para consultar um documento?
db.collectio.find({});

###### MongoDB tem suporte a SQL?
Não, ele tem linguagem própria

###### Quais os tipos de banco NoSql?
Documentos, Chave-Valor, Grafo e Coluna/Família de Colunas
