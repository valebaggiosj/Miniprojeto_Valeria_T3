# **Mini-Projeto Avaliativo para o curso de Visualização de Dados e BI (Módulo 1) do programa SCTEC/2026.**

Entregar um script em Python que realize uma Análise Exploratória da base Varejo seguindo etapas claras, documentadas e reproduzíveis.

Etapas obrigatórias:
* Carregar a base Varejo.csv com pandas e mostrar: número de registros, colunas e tipos de dados.
* Verificar e reportar ao menos dois problemas básicos: valores nulos por coluna, duplicatas e possíveis inconsistências (ex.: datas inválidas ou categorias vazias).
* Fazer as três etapas de limpeza mínima necessária: remover ou imputar nulos (explique a escolha), eliminar duplicatas relevantes e ajustar tipos de dados (ex.: converter coluna DATA para datetime).
* Gerar estatísticas descritivas básicas para coluna de número de filhos do cliente (média; mediana; desvio padrão; moda; máximo; mínimo; e contagem).
* Explorar padrões de agrupamento com pelo menos dois agrupamentos (por exemplo: gênero com mais vendas, compras), usando groupby() ou pivot_table().
* Produzir um pequeno bloco de conclusões (3–6 tópicos) com os principais insights obtidos e possíveis problemas remanescentes na base.

DATASET 
Base Varejo
https://www.kaggle.com/datasets/namespaiva/base-varejo/data

O dataset possui um total de 830.000 registros, dos quais 96.553 eram registros duplicados, e 4 colunas estavam totalmente vazias. O nome das colunas foi alterado, pois não deixava bem claro o dado que cada uma trazia. 

Foram realizados os procedimentos básicos de limpeza da base:
- Alteração do nome das colunas
- Exclusão de registros duplicados
- Retirado possível espaço em brando nos dados de texto
- Para tipos numéricos, não vi necessidade de fazer alterações, pois já estavam como dados inteiros
- Não achei informações que se referissem ao mesmo produto e categoria mas com escrita diferente
- O campo data foi alterado para tipo datetime para facilitar posterior manipulação
- As colunas vieram sem dados nulos/vazios, tirando as 4 últimas colunas que foram excluidas do dataframe.
- Foram atualizados os dados da coluna de Estado Civil para visualizar diretamente a descrição de cada Estado Civil, e não os números, o que dificultava o entendimento.

Análise do dataset através de relatórios, mostrando a relação em quantidade de registros, e gráficos para visualizar a distribuição desses dados. Segue a análise dessa exploração de conjunto de dados:
- A maioria das compras é feita pelo sexo Feminino, pouco mais da metade.
- A categoria de produtos mais vendidos é a de Alimentos, mais do dobro que produtos de Higiene e Limpeza.
- O produto mais vendido é Presunto Cozido
- Vendas por ano: A venda por está bastante similar, variando entre 20% a 30%, sendo 2021 o melhor ano e o que menos vendeu foi 2022.
- Vendas por mês: O que mais chamou a atenção foi o mês de Novembro que deu um total menor a 5% das vendas, comparando com os outros meses que deu entre 7,76 e 10,11%%. Além do agrupamento, acabei montando 2 gráficos para continuar analisando a venda de produtos.
- Quantidade de filhos e compras: Nesta relação, mais da metade das compras é feita por pessoas sem filhos. A princípio, tendo mais pessoas na família, o consumo tende a aumentar. Por isso, seria interessante ter mais informações para entender melhor a quê se deve isso e se o valor gasto segue a mesma porcentagem ou não. 
- Gráfico linear para visualizar a evolução das compras ao longo dos meses e anos. Notam-se muitos altos e baixos, mostrando que as vendas mudam a cada mês, sem muita constância. Podemos ver que tem meses com aumento em venda de produtos (04/2019, 11/2019 (observando que novembro, em geral, estava com registro de vendas mais baixo) e 09/2021) e teve algumas quedas maiores em 10/2021 e 08/2022 (mês com menor venda). 
- Gerado um gráfico de barras mostrando a comparação dos meses nos diferentes anos e também tem um acompanhamento linear com a soma de vendas dos meses. Notamos que ao longo de um ano, aos poucos as vendas vão diminuíndo, tendo um aumento em maio e uma queda mais brusca em novembro, e dezembro já volta a subir. 
- Gráfico de barras (histograma) para visualizar como eram as compras entre o sexto Feminino e Masculino. Não há uma diferença muito visível para nenhuma categoria de produtos. Já na contagem de registros de venda geral, o público feminino tinha maior registro de compras, mas não era uma grande diferença. E novamente, detaca-se aqui a venda maior na categroia de alimentos.


De forma geral, o dataset teria sido interessante poder ter acesso a dados como custo de produtos e valor das compras para analisar com maior profundidade a parte financeira desse setor de varejo.


