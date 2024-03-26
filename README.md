# LPED-Disciplina-03-Trabalho

## Descrição do Projeto
Este projeto tem como objetivo realizar a leitura e compressão dos dados dos endereços, que estarão após o processo, disponíveis no formato .parquet. Os dados serão persistidos localmente utilizando API em Python do Duck DB como base de dados. A fonte dos dados é o Instituto Brasileiro de Geografia e Estatística (IBGE).

Os dados locais estão atualmente armazenados em formato .CSV

Este trabalho foi desenvolvido por W. Carvalho em 2024.

## Fonte de Dados
- **Origem**: IBGE
- **Formato, Compressão**: .parquet
- **Armazenamento Local para Leitura**: CSV

### Data/ Armazenamento após processamento e compressão.
### Pipe/ Arquivos Locais .csv
### ibge.db / DuckDB

### Referencia Local
![Ref](image.png)


######
### Desafios: 
- Como orientação, as dificuldades da implementação são a utilização em memória do duckdb, é preciso monitorar a capacidade, operar com cuidado, ativar as dependências para persistencia local caso queira persistir os dados.
- Uma outra forma de operarmos neste caso, seria construindo um script em python onde podemos utilizar da biblioteca csv ou pandas, unificando-os e escrevendo em .parquets
- O intuito em não utilizar o pandas nos favorece a visualizar outras possibilidades analíticas.

### Oportunidades de Melhorias:

- como a API do duckdb para persistencia analitca, como melhorias também poderiamos utilizar a leitura direta via API diretamente do IBGE, obtivemos um ganho substancial em leitura e escrita de forma a satisfazer o objeto de estudo, 111 mi de registros em segundos.
- Verificar as atualizações, persistir e orquestrar, processar com outras tecnologias, airflow, databricks, spark.

###### Resultados obtidos  em armazenamento, após compressão:

| Armazenamento  | Tipo Dado   |
| ------------ | ------------ |
| 3,9 GB   |   CSV |
|  1,4 GB   |   .Parquet |




``Documentação utilizada no projeto``


[https://duckdb.org/docs/guides/index](https://duckdb.org/docs/guides/index)
[https://duckdb.org/docs/data/partitioning/partitioned_writes](https://duckdb.org/docs/data/partitioning/partitioned_writes)
[https://duckdb.org/docs/guides/import/csv_import](https://duckdb.org/docs/guides/import/csv_import)

