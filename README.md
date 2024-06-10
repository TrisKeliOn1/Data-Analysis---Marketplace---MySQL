<h1 align="center"> Análise de Dados de vendas de um mercado </h1>

<p align="center">
  <a href="#-sobre">Sobre</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-objetivo-do-projeto">Objetivo do Projeto</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#lista-de-análise">Lista de Análise</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;<br>
  <a href="#abordagem-usada">Abordagem Usada</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-perguntas-de-negócios-para-responder">Perguntas de negócios</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-cálculos-de-receita-e-lucro">Cálculos de Receita e Lucro</a>
</p>

## 🚀 Sobre

<p align="center">
Este projeto tem como objetivo explorar os dados de vendas do mercado para entender filiais e produtos de melhor desempenho, tendências de vendas de diferentes produtos e comportamento do cliente. O objetivo é estudar como as estratégias de vendas podem ser melhoradas e otimizadas. O conjunto de dados foi obtido da competição Kaggle Walmart Sales Forecasting.
</p>

## 🚀 Objetivo do Projeto

<p align="center">
O principal objetivo deste projeto é compreender os diferentes fatores que afetam as vendas das diferentes filiais.
</p>

### Lista de Análise:

- **Análise de produto** <br>
Realize análises dos dados para compreender as diferentes linhas de produtos, as linhas de produtos com melhor desempenho e as linhas de produtos que precisam ser melhoradas.

- **Análise de vendas** <br>
Esta análise visa responder à questão das tendências de vendas do produto. O resultado disso pode ajudar a medir a eficácia de cada estratégia de vendas que a empresa aplica e quais modificações são necessárias para obter mais vendas.

- **Análise do cliente** <br>
Esta análise visa descobrir os diferentes segmentos de clientes, as tendências de compra e a rentabilidade de cada segmento de clientes.

### Abordagem Usada
- Organização de dados: Esta é a primeira etapa em que a inspeção dos dados é feita para garantir que valores NULL e valores ausentes sejam detectados e métodos de substituição de dados sejam usados ​​para substituir valores ausentes ou NULL.<br>

    - Construa um banco de dados 
    - Crie a tabela e insira os dados.
    - Selecione colunas com valores nulos. Não há valores nulos em nosso banco de dados, pois na criação das tabelas, definimos NOT NULL para cada campo, portanto, os valores nulos são filtrados.

- Engenharia de recursos: isso ajudará a gerar algumas novas colunas a partir das existentes.

    - Adicione uma nova coluna chamada time_of_day para fornecer informações sobre as vendas pela manhã, tarde e noite. Isso ajudará a responder à pergunta em que parte do dia é realizada a maior parte das vendas.
    - Adicione uma nova coluna chamada day_name que contém os dias extraídos da semana em que a transação ocorreu (segunda, terça, quarta, quinta, sexta). Isso ajudará a responder à pergunta sobre qual semana do dia cada filial está mais movimentada.
    - Adicione uma nova coluna chamada month_name que contém os meses extraídos do ano em que a transação ocorreu (janeiro, fevereiro, março). Ajude a determinar qual mês do ano tem mais vendas e lucro.

- Análise Exploratória de Dados (EDA): A análise exploratória de dados é feita para responder às questões e objetivos listados neste projeto.<br>


## 🚀 Perguntas de negócios para responder

### Perguntas genérica
- Quantas cidades únicas os dados têm?
- Em qual cidade fica cada filial?

### Produtos
- Quantas linhas de produtos exclusivas os dados possuem?
- Qual é o método de pagamento mais comum?
- Qual é a linha de produtos mais vendida?
- Qual é a receita total por mês?
- Qual mês teve o maior CPV?
- Qual linha de produtos teve a maior receita?
- Qual é a cidade com maior receita?
- Qual linha de produtos teve o maior IVA?
- Busque cada linha de produtos e adicione uma coluna a essas linhas de produtos mostrando "Bom", "Ruim". Bom se for maior que as vendas médias
- Qual filial vendeu mais produtos do que a média dos produtos vendidos?
- Qual é a linha de produtos mais comum por gênero?
- Qual é a avaliação média de cada linha de produto?

### Vendas
- Número de vendas realizadas em cada horário do dia por dia da semana
- Qual dos tipos de clientes gera mais receita?
- Qual cidade tem a maior porcentagem de imposto/IVA (Imposto sobre Valor Agregado)?
- Que tipo de cliente paga mais IVA?

### Cliente

- Quantos tipos de clientes exclusivos os dados possuem?
- Quantos métodos de pagamento exclusivos os dados possuem?
- Qual é o tipo de cliente mais comum?
- Qual tipo de cliente compra mais?
- Qual é o sexo da maioria dos clientes?
- Qual é a distribuição de género por ramo?
- Em que horário do dia os clientes dão mais avaliações?
- Em que horário do dia os clientes dão mais avaliações por agência?
- Qual dia da semana tem as melhores classificações médias?
- Qual dia da semana tem as melhores avaliações médias por agência?

## 🚀 Cálculos de receita e lucro
$ CPV = unidadesPreço * quantidade $

$ IVA = 5% * CPV $

O IVA é adicionado ao CPV e é isso que é cobrado do cliente.

$ total(vendas Brutas) = ​​IVA + CPV $

$ lucro bruto (receita Bruta) = total (vendasBrutas) - CPV $

Margem Bruta é o lucro bruto expresso em porcentagem do total (lucro/receita Bruta)

$ \text{Margem Bruta} = \frac{\text{receita Bruta}}{\text{receita Total}} $

Exemplo com a primeira linha do nosso banco de dados:

Dados fornecidos:

$ \text{Preço unitário} = 45,79 $
$ \text{Quantidade} = 7 $
$ CPV = 45,79 * 7 = 320,53 $

$\text{IVA} = 5% * CPV\= 5% 320,53 = 16,0265 $

$ total = IVA + CPV\= 16,0265 + 320,53 = 

$ \text{Porcentagem da margem bruta} = \frac{\text{renda bruta}}{\text{receita total}}\=\frac{16,0265}{336,5565} = 0,047619\\aproximadamente 4,7619% $









