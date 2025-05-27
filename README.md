# Análise de Desempenho de Lojas com Foco Geográfico para Decisão de Venda

## 📋 Descrição do Projeto
Este projeto analisa o desempenho de quatro lojas (Loja 1, Loja 2, Loja 3, Loja 4) para recomendar ao Senhor João qual delas vender, com base em métricas financeiras, de satisfação do cliente, eficiência logística e padrões geográficos. As análises incluem faturamento total, categorias e produtos mais/menos vendidos, média das avaliações, custo médio de frete, e distribuição geográfica das vendas usando coordenadas (`lat`, `lon`). O projeto utiliza Python no Google Colab, com bibliotecas como `pandas`, `matplotlib`, `seaborn`, e `folium`, para gerar visualizações que embasam a decisão.

## 🎯 Objetivo
O objetivo é identificar a loja com pior desempenho combinado (baixo faturamento, avaliações ruins, frete elevado, e baixa densidade de vendas em regiões estratégicas) para recomendar sua venda. As análises geográficas complementam a decisão, revelando se a localização das vendas influencia o desempenho.

## 📊 Datasets
Os dados são provenientes de quatro arquivos CSV hospedados no GitHub:
- `loja_1.csv`
- `loja_2.csv`
- `loja_3.csv`
- `loja_4.csv`

Cada dataset contém:
- **Produto**: Nome do produto vendido.
- **Categoria do Produto**: Categoria do produto.
- **Preço**: Valor da venda.
- **Frete**: Custo do frete.
- **Data da Compra**: Data da transação.
- **Vendedor**: Nome do vendedor.
- **Local da compra**: Local da transação.
- **Avaliação da compra**: Nota do cliente.
- **Tipo de pagamento**: Método de pagamento.
- **Quantidade de parcelas**: Número de parcelas.
- **lat, lon**: Coordenadas geográficas.

## 🛠️ Metodologia
O projeto foi implementado em Python no Google Colab, com as seguintes etapas:
1. **Carregamento e Consolidação**: Os datasets foram consolidados em um DataFrame com a coluna `Loja`.
2. **Análises Realizadas**:
   - **Faturamento Total**: Soma de `Preço` por loja.
   - **Categorias Mais/Menos Vendidas**: Contagem de vendas por `Categoria do Produto`.
   - **Média das Avaliações**: Média de `Avaliação da compra`.
   - **Produtos Mais/Menos Vendidos**: Contagem de vendas por `Produto`.
   - **Custo Médio de Frete**: Média de `Frete`.
   - **Análise Geográfica**: Agrupamento por `lat` e `lon` para calcular vendas, faturamento e avaliações por localização.
3. **Visualizações**:
   - **Gráfico de Barras**: Compara faturamento total por loja.
   - **Gráfico de Pizza**: Mostra distribuição de avaliações.
   - **Gráfico de Linha**: Compara avaliações e frete.
   - **Gráfico de Dispersão**: Mostra vendas por localização (`lat`, `lon`).
   - **Mapa de Calor**: Exibe concentração de vendas por região.
4. **Recomendação**: Identifica a loja com pior desempenho para venda.

## 📈 Visualizações
Os gráficos incluem:
- **Barras (Faturamento Total)**: Compara receita por loja.
- **Pizza (Média das Avaliações)**: Mostra proporção de satisfação.
- **Linha (Avaliações e Frete)**: Compara satisfação e custo logístico.
- **Dispersão (Vendas por Localização)**: Exibe vendas por coordenadas, com tamanhos proporcionais.
- **Mapa de Calor**: Destaca áreas com maior densidade de vendas.

A paleta `viridis` garante legibilidade e consistência.

## 📝 Recomendação
Recomenda-se vender a loja com pior desempenho combinado, hipoteticamente a **Loja 3**, caso apresente:
- **Baixo faturamento**: Menor receita (gráficos de barras/pizza).
- **Avaliações ruins**: Menor média de avaliações (gráfico de pizza/linha).
- **Frete elevado**: Maior custo logístico (gráfico de linha).
- **Baixa densidade geográfica**: Vendas concentradas em áreas menos estratégicas (dispersão/mapa de calor).

Vender a Loja 3 libera capital para investir em lojas mais promissoras, como a Loja 1, com alto faturamento, boas avaliações, frete competitivo, e vendas em regiões de alta densidade.

## 🚀 Como Executar
1. **Pré-requisitos**:
   - Google Colab com internet.
   - Bibliotecas: `pandas`, `matplotlib`, `seaborn`, `folium` (instale `folium` com `!pip install folium` no Colab).
2. **Passos**:
   - Abra o Google Colab.
   - Copie e cole os códigos do repositório em células.
   - Execute com `Shift + Enter` para gerar tabelas, gráficos e o mapa de calor (HTML).
3. **Arquivos Gerados**:
   - CSVs: `metricas_por_loja.csv`, `vendas_por_local.csv`, etc.
   - HTML: `mapa_calor_vendas.html` (mapa de calor).

## 📂 Estrutura do Repositório
- `Consolidacao_Analises_e_Graficos.py`: Análises principais e gráficos.
- `Analise_Geografica_Vendas.py`: Análise geográfica com dispersão e mapa de calor.
- `README.md`: Descrição do projeto.

## 💡 Insights
- Lojas com vendas concentradas em áreas urbanas (mapa de calor) podem ter maior potencial.
- Fretes elevados podem estar ligados a localizações geográficas distantes (verificar com `lat`, `lon`).
- Lojas com avaliações altas e vendas diversificadas são mais valiosas.
