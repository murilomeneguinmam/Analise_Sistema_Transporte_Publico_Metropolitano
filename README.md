# Análise do Sistema de Transporte Público Metropolitano

# Contexto do projeto
Este projeto tem como objetivo a análise de dados de bilhetagem eletrônica do transporte público da cidade de São Paulo, disponibilizados publicamente pela SPTrans.

A análise busca compreender padrões de demanda, volume de passageiros, comportamento temporal e possíveis oportunidades de otimização operacional, utilizando dados históricos extraídos em formato XLS/XLSX.

Os dados são coletados via scripts em Python e ingeridos em uma camada RAW no Databricks. O processamento segue a arquitetura Medallion (Bronze, Silver e Gold), garantindo organização, qualidade e confiabilidade das informações até a camada analítica.

Após o tratamento e modelagem dimensional dos dados, são construídos indicadores de desempenho (KPIs) e dashboards no Power BI, com foco em apoiar a tomada de decisão baseada em dados no contexto do transporte público metropolitano.

# Definição do Problema (Análise de Lacunas)
O sistema de transporte público demanda monitoramento contínuo para garantir eficiência operacional, equilíbrio entre oferta e demanda e sustentabilidade financeira.

A partir dos dados de bilhetagem eletrônica, este projeto busca responder às seguintes questões analíticas:

Total de passageiros transportados

Como o volume de passageiros se comporta entre dias úteis, finais de semana e feriados?

Média de passageiros transportados

Quantidade de linhas

Quantidade de empresas operando

Quais linhas concentram maior volume de passageiros?

Como o volume de passageiros se comporta entre dias úteis, finais de semana e feriados?

Quais padrões podem indicar necessidade de ajuste operacional?

O objetivo é transformar dados operacionais em informação estratégica, apoiando decisões relacionadas à alocação de frota, planejamento de horários e análise de desempenho.
