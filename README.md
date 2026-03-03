# Análise do Sistema de Transporte Público Metropolitano

# Contexto do projeto
Este projeto tem como objetivo a análise de dados de bilhetagem eletrônica do transporte público da cidade de São Paulo, disponibilizados publicamente pela SPTrans.

A análise busca compreender padrões de demanda, volume de passageiros, comportamento temporal e possíveis oportunidades de otimização operacional, utilizando dados históricos extraídos em formato XLS/XLSX.

Os dados são coletados via scripts em Python e ingeridos em uma camada RAW no Databricks. O processamento segue a arquitetura Medallion (Bronze, Silver e Gold), garantindo organização, qualidade e confiabilidade das informações até a camada analítica.

Após o tratamento e modelagem dimensional dos dados, são construídos indicadores de desempenho (KPIs) e dashboards no Power BI, com foco em apoiar a tomada de decisão baseada em dados no contexto do transporte público metropolitano.




