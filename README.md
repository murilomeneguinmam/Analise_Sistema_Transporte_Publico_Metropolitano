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

 ### Quais linhas concentram maior volume de passageiros ao longo do período analisado?

Existe sazonalidade na demanda considerando variações mensais e diárias?

Quantas linhas operam em nível crítico de ocupação (superlotação)?

Como a taxa média de ocupação se comporta ao longo do tempo?

Há concentração de demanda por grupos estruturais de linhas?

O objetivo é apoiar o planejamento operacional e o capacity planning do sistema, fornecendo indicadores que permitam identificar desequilíbrios na distribuição da frota, monitorar criticidade operacional e embasar decisões orientadas a dados.

 # Arquitetura do processo de ingestão

 
🔹 Camada RAW

Armazenamento dos arquivos originais extraídos em formato XLS/XLSX.

🔹 Camada Bronze

Conversão e padronização inicial dos dados, com tipagem e tratamento básico de inconsistências.

🔹 Camada Silver

Aplicação de regras de negócio, limpeza avançada, normalização e preparação para análise.

🔹 Camada Gold

Modelagem dimensional (Star Schema), construção da tabela fato e dimensões analíticas.
 
