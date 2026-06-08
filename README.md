# 📊 Tratamento e Análise de Dados — Campe Supply

Projeto desenvolvido durante a capacitação de Ciência de Dados da **Asimov Jr.**, com foco em 
tratamento de dados corrompidos e análise exploratória de dados de vendas.

---

## 🛠️ Tecnologias Utilizadas

| Biblioteca | Finalidade |
|---|---|
| `pandas` | Manipulação e análise de dados |
| `numpy` | Operações numéricas |
| `matplotlib` | Criação dos gráficos |
| `difflib` | Correção de erros de digitação por similaridade de texto |

---

## 🔍 Análise Exploratória dos Dados

Iniciei o notebook importando as bibliotecas necessárias (`pandas` e `numpy`) e carregando 
a planilha diretamente do Google Drive. Em seguida, realizei uma análise exploratória para 
conhecer melhor os dados antes de iniciar o tratamento. Utilizei `info()`, `isnull().sum()`, 
`value_counts()` e `describe()` para entender a estrutura da planilha — tipos de dados, 
valores ausentes e distribuição das categorias. Essa etapa foi essencial para planejar 
as correções necessárias.

---

## 🧹 Tratamento dos Dados

O tratamento seguiu as seguintes etapas:

1. **Exclusão de colunas inválidas** — removidas as colunas sem valor analítico
2. **Renomeação das colunas** — padronização dos nomes para facilitar a leitura
3. **Conversão dos tipos de dados** — colunas numéricas convertidas para `float` e datas para `datetime`
4. **Correção de erros de digitação** — utilizada a função `get_close_matches` da biblioteca `difflib` 
para corrigir inconsistências nas colunas categóricas por similaridade de texto
5. **Tratamento de valores ausentes** — foi criada uma função para centralizar o tratamento:

| Coluna | Tratamento |
|---|---|
| Data de Venda | Preenchida com a data anterior (forward fill) |
| Margem de Lucro e Lucro | Preenchidas com a mediana |
| Colunas categóricas | Preenchidas com a moda |
| Faturamento | Linhas removidas |

Após o tratamento, o dataset foi verificado e exportado.

---

## 📈 Análise dos Dados

A análise foi iniciada pelo faturamento por diferentes dimensões, para ter um panorama geral do negócio:

- 📅 Faturamento Mensal
- 🏷️ Faturamento por Setor
- 📦 Faturamento por Produto
- 🗺️ Faturamento por Região
- 📍 Faturamento por Estado
- 👤 Faturamento por Vendedor

Em seguida, foram exploradas análises complementares:

- 💰 Margem de Lucro por Produto
- 🏪 Distribuição do Faturamento por Setor e Canal de Venda
- 🎯 Ticket Médio por Tipo de Cliente

Cada tipo de gráfico foi escolhido conforme o objetivo da visualização:

| Gráfico | Quando usar |
|---|---|
| Barras horizontais | Comparar muitas categorias |
| Colunas | Comparar valores entre categorias |
| Pizza | Mostrar proporção de um todo |
| Linhas | Mostrar evolução ao longo do tempo |
| Colunas empilhadas | Mostrar composição de um total |
---

## 👩‍💻 Autora

**Ana Beatriz Mendes de Sousa**  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/ana-beatriz-mendes-de-sousa)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=flat&logo=github&logoColor=white)](https://github.com/beatrizzmendees)
