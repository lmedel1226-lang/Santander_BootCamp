Projeto ETL – Análise de Investimento por Cliente (Anúncios Meta)

Este projeto demonstra a implementação de um pipeline ETL (Extract, Transform, Load) aplicado a um cenário de negócios envolvendo clientes que contratam serviços de anúncios na plataforma Meta (Facebook/Instagram).

O objetivo principal é simular dados de investimento em mídia, processá-los de forma estruturada e gerar indicadores agregados que possam apoiar análises financeiras e decisões estratégicas.

Descrição do Fluxo

O pipeline é dividido em quatro etapas principais:

1. Geração de Dados Sintéticos

São gerados dados artificiais representando investimentos (spend) realizados por diferentes clientes (client_id).
Os dados são salvos em um arquivo CSV, simulando um cenário realista de compras de mídia, incluindo alguns registros inválidos para fins de validação e limpeza.

2. Extract (Extração)

O arquivo CSV é lido e carregado em memória.
Nesta etapa, são realizadas verificações iniciais, como:

existência do arquivo,

presença das colunas obrigatórias,

contagem de registros.

3. Transform (Transformação)

Os dados passam por um processo de limpeza e validação:

remoção de registros com identificador de cliente inválido,

descarte de valores nulos, não numéricos ou negativos de investimento.

Após a validação, os dados são agregados para calcular a média de investimento por cliente, representando o gasto médio em anúncios na plataforma Meta.

4. Load (Carga)

O resultado final é persistido em um arquivo JSON, contendo a média de investimento para cada cliente, pronto para consumo por dashboards, APIs ou análises posteriores.

Estrutura de Arquivos

meta_clientes.csv
Arquivo CSV contendo os dados sintéticos de investimento por cliente.

resultado_media_por_cliente.json
Arquivo JSON com a média de investimento calculada para cada cliente.

notebook.ipynb
Notebook com todo o processo de geração, tratamento, análise e exportação dos dados.

Tecnologias Utilizadas

Python 3

Pandas

NumPy

JSON

Jupyter Notebook

Objetivo Educacional

Este projeto tem caráter didático e foi desenvolvido para demonstrar:

boas práticas de processamento de dados,

aplicação do conceito ETL,

validação e limpeza de dados,

agregação de métricas de negócio em um contexto de marketing digital.

Os dados utilizados são totalmente sintéticos e não representam informações reais de clientes ou investimentos.