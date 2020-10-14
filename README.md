# Desafio Final do curso de Desenvolvimento de Business Intelligence do IGTI

Consulta dos dados no MySql: foi utilizado uma versão portable do mysql, com unicontroller e HeidiSQL

Utilizado Pentaho 9.0

Job possui todas as transformações feitas para criação dos DW e da tabela fato.
DW: Custumers, orders, products. 
Fato: Sales

Caso aconteça algum erro durante a execução desse Job ou nas transformações será enviado um email com o log


## Resumo

Os dados estavam armazenados inicialmente num banco de dados MySQL, foi feita a extração para o pentaho, tratados, feita a automação com jobs e, no final de cada tratamento enviados para um bucket no S3 da Amazon AWS. Por fim, foi criado um Crawler para transformar o Bucket em DW na nuvem e, utilizando o Athena e um conector JDBC, foi feita a conexão no PowerBI para a criação de Dashboards.


## Entendendo os Arquivos

.ktr são as transformações no pentaho
.kjb job contendo todas as transformações encapsuladas
.pbix dashboard criado no PowerBI
.sql banco de dados MySQL
