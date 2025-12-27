# Alura_Store

 
## Descrição
Neste projeto irei ajudar o Senhor João a decidir qual loja da sua rede vender, analisando dados de vendas, desempenho e avaliações de suas 4 lojas. O objetivo é identificar a loja com menor eficiência e apresentar uma recomendação final baseada nos dados.


## Conhecendo os dados
Iniciei o projeto realizando checagens exploratórias para compreender e visualizar o conjunto de dados.   

Nessa etapa, obtive informações como:
* estrutura da base de dados
* número de linhas e colunas
* nomes das variáveis
* tipos de dados
* valores presentes 

Além disso, verifiquei a existência de valores nulos e registros duplicados, garantindo uma compreensão inicial da qualidade dos dados.


## Métodos utilizados na exploração dos dados:
### Visualizando as primeiras linhas do DataFrame:
```python
loja2.head()
```
### Obtendo informações gerais:
```python
loja2.info()
```
### Obtendo número de linhas e colunas:
```python
loja2.shape
```
### Calculando estatísticas descritivas:
```python
loja2.describe()
```
### Identificando valores nulos:
```python
loja2.isnull().sum()
```
### Identificando valores duplicados:
```python
loja2.duplicated().sum()
```
  
## Analisando os dados
Em seguida comecei a análise mais detalhada dos nossos conjuntos de dados.

Nessa etapa, calculei:
* O faturamento total de cada loja, com o objetivo de comparar qual apresenta o maior faturamento.
* A quantidade de produtos vendidos por categoria em cada loja.
* Criei um gráfico de barras agrupadas comparando as categorias de produtos mais vendidas por loja

### Calculando faturamento total por loja:
```python
faturamento_loja = loja['Preço'].sum()
print(f'Faturamento loja R${faturamento_loja:,.2f}')
```

### Calculando a quantidade de produtos mais vendidos por categoria em cada loja
```python
qtd_vendas_cat_loja1 = loja1['Categoria do Produto'].value_counts()
qtd_vendas_cat_loja1
```
### Criando o gráfico de barras agrupadas para comparar a categoria de produtos mais vendidos
```python
df_vendas_por_categoria.plot(kind='bar', figsize= (10, 5))
```
