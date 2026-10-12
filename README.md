# Segmentação de Clientes para CRM | Olist

Em quem investir a verba de CRM quando 97% dos clientes compraram uma única vez.

Mini projeto de análise de dados conduzido com CRISP-DM, usando o dataset público de e-commerce da Olist. Toda a segmentação foi calculada manualmente com pandas, sem bibliotecas de machine learning.

## Contexto (cenário fictício)

A gerência de CRM tem verba para campanhas de relacionamento no próximo trimestre e quer saber em quem investir primeiro.

**Pergunta de negócio:** como segmentar a base de clientes para direcionar as campanhas?

## Principais resultados

- De 93.104 clientes (jan/2017 a ago/2018), apenas 3% voltaram a comprar. Esses recorrentes representam 5,6% da receita.
- Quem volta gasta o dobro no período (R$ 309 vs R$ 161), não por comprar mais caro, mas por comprar de novo. O problema de negócio passa a ser a falta da segunda compra.
- Prioridade alta: 7.145 clientes de compra única com última compra há até 92 dias e gasto acima de R$ 132.
- No cenário moderado, cada cliente de prioridade alta impactado gera R$ 10,05 de receita esperada, 5x mais que a prioridade baixa. Prioridades alta e média somam cerca de R$ 163 mil em receita potencial.
- Entrega: lista de 25.232 clientes ordenada por prioridade, em CSV no padrão do Excel brasileiro.

## Limitações

- Taxas de conversão são premissas, não dados observados.
- Valores são receita, não margem.
- O ganho real deve ser medido com grupo de controle (teste A/B).

## Etapas do notebook

1. Compreensão do negócio
2. Entendimento dos dados (clientes, pedidos e pagamentos)
3. Preparação: pedidos entregues, valor por pedido, cliente real (`customer_unique_id`)
4. RFM: recência e valor em quintis, frequência como corte binário (compra única vs recorrente)
5. Priorização e cenários de receita
6. Entrega: lista da campanha e resumo executivo

## Como reproduzir

1. Baixe o dataset no Kaggle: [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
2. Salve os CSVs em uma pasta `raw/` dentro da pasta do projeto
3. Ajuste a variável `PASTA_RAIZ` na primeira célula do notebook para o caminho da sua pasta
4. Execute as células em ordem

## Ferramentas

Python, pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook.

## Autor

Fabio Oliveira | Analista de Dados
