# Análise do Sistema de Transporte Público Metropolitano

# Contexto do projeto
Este projeto tem como objetivo a análise de dados de bilhetagem eletrônica do transporte público da cidade de São Paulo, disponibilizados publicamente pela SPTrans.

A análise busca compreender padrões de demanda, volume de passageiros, comportamento temporal e possíveis oportunidades de otimização operacional, utilizando dados históricos extraídos em formato XLS/XLSX.

Os dados são coletados via scripts em Python e ingeridos em uma camada RAW no Databricks. O processamento segue a arquitetura Medallion (Bronze, Silver e Gold), garantindo organização, qualidade e confiabilidade das informações até a camada analítica.

Após o tratamento e modelagem dimensional dos dados, são construídos indicadores de desempenho (KPIs) e dashboards no Power BI, com foco em apoiar a tomada de decisão baseada em dados no contexto do transporte público metropolitano.

# Definição do Problema.
O transporte público metropolitano opera sob alta variabilidade de demanda, exigindo monitoramento contínuo para garantir eficiência operacional, equilíbrio de capacidade e qualidade do serviço prestado à população.

A partir dos dados de bilhetagem eletrônica, este projeto busca analisar o comportamento da demanda e os níveis de ocupação das linhas, com foco em identificar padrões operacionais e possíveis gargalos de capacidade.

As principais questões analíticas abordadas são:

 #### Quais linhas concentram maior volume de passageiros ao longo do período analisado?

 #### Existe sazonalidade na demanda considerando variações mensais e diárias?

 #### Quantas linhas operam em nível crítico de ocupação (superlotação)?

 #### Como a taxa média de ocupação se comporta ao longo do tempo?

 #### Há concentração de demanda por grupos estruturais ?

O objetivo é apoiar o planejamento operacional e o capacity planning do sistema, fornecendo indicadores que permitam identificar desequilíbrios na distribuição da frota, monitorar criticidade operacional e embasar decisões orientadas a dados.

# Arquitetura do processo de ingestão

#### Camada RAW
📁 VOLUMES

 raw_sptrans/ Armazenamento dos arquivos originais extraídos em formato XLS/XLSX.

🗄️ DATABASES (Unity Catalog)
#### Camada Bronze
sptrans_bronze/ bronze_bilhetagem_diario / 
Delta Table-união de todos os XLS/XLSX, dados raw unificados, com limpeza mínima remoção de headers irrelevantes, colunas vazias. 

#### Camada Prata
sptrans_silver/ silver_bilhetagem_diario / 
Delta Table-Dados limpos, padronizados, data extraída, cabeçalhos repetidos removidos.

#### Camada Ouro
sptrans_gold/ fato_passageiros_diario / dim_calendario / dim_empresa / dim_grupo / dim_linha / dim_lote / dim_tipo_passageiros / 
Modelagem dimensional (Star Schema), Tabela fato e dimensões analíticas.
 
![Arquitetura_Sistema de transporte Público Metropolitano](https://github.com/user-attachments/assets/87a39d73-9a7a-47e8-970e-a07a84579dcf)
