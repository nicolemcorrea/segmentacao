
# Segmentação RFM e Análise de Cohort 📈

<details>
  <summary><strong style="font-size: 16px;">Objetivo</strong></summary>

O objetivo deste projeto foi aplicar a Segmentação RFM e a Análise e Cohort numa base de dados de clientes de um supermercado fictício chamado “O Mercado”, com o intuito de aprofundar a compreensão dos clientes, permitindo que este estabelecimento personalize suas estratégias de marketing e vendas para atender às necessidades específicas de cada grupo de clientes de forma eficaz, além de identificar padrões de diferenças comuns e significativas entre os clientes.
</details>

<details>
  <summary><strong style="font-size: 16px;">Equipe</strong></summary>
Nicole Machado Corrêa.
</details>

<details>
  <summary><strong style="font-size: 16px;">Ferramentas e Tecnologias</strong></summary>
Para a análise exploratória dos dados, foi utilizada a ferramenta Google Sheets. Já para a visualização de dados, foi utilizado o Looker Studio. Por fim, para a apresentação dos resultados utilizou-se o Google Slides.
</details>

<details>
  <summary><strong style="font-size: 16px;">Processamento e Análises</strong></summary>

A primeira etapa deste trabalho foi a limpeza e tratamento dos dados que seriam utilizados posteriormente nas análises. Inicialmente, foi calculado a idade dos clientes deste banco de dados e, para tanto, optou-se por não considerar os dados de clientes com idade superior a 121 anos, pois estes dados poderiam não ser representativos. Além disso, também foram descartados os dados de transações duplicadas para o mesmo cliente. Para esta análise, também se observou que havia clientes que não possuíam salários cadastrados (representando cerca de 1% de todos os dados), mas as demais informações de cadastro estavam presentes. Sendo assim, considerou-se utilizar a mediana dos salários para estes dados faltantes, sendo criada a variável “salario_corrigido”. 
Após isso, foi feita a integração das planilhas “clientes”, resumo_compras” e “transacoes”. Após esta etapa, verificou-se que haviam clientes que possuíam resumo de compras, porém não possuíam transações. Desta forma, também optou-se por retirar os dados destes clientes, pois futuramente estes valores iriam afetar a análise de segmentação. Após este processo, e para auxiliar em análises futuras, algumas variáveis foram criadas, como o total de compras por cliente, a contagem de transações por cliente e a data da última compra por cliente. Com estas informações também foi possível calcular quantos dias haviam se passado desde a última compra do cliente.

Com base nestas informações da tabela integrada e as variáveis criadas adicionalmente, foi criada uma tabela dinâmica com todos os dados. Com esta etapa concluída, partiu-se para a fase de representar estas informações em gráficos simples, para compor um dashboard.
Com o dashboard concluído, iniciou-se uma nova etapa da análise, que foi a criação de quartis e percentis, para “dividir” nossas variáveis em cem partes, cada uma com um percentual de dados igual. Ela será fundamental para a análise de segmentação de clientes. Para isto, foi utilizada uma planilha dinâmica contendo o “id_cliente”, a contagem de transações por cliente (frequência – F), o total monetário gasto por cada cliente (monetary – M) e a quantidade de dias correspondente a última compra do cliente (recência – R). A estes três valores – R, F e M – serão atribuídos “scores” com base nos percentis calculados.
Optou-se nesta análise utilizar os valores de cinco percentis, onde cada percentil representava 20% dos nossos dados. O cálculo dos quartis também foi feito, mas apenas para nível de aprendizado. Feito isto, aplicou-se então a técnica de análise RFM, com 10 categorias de segmentação de clientes (as categorias foram atribuídas de cordo com o link: 
Com os clientes já separados em categorias, passou-se para a fase da análise de cohort, para visualizarmos a retenção deste grupo de clientes ao longo do tempo. Para isso, considerou-se a diferença entre a data da compra do cliente e a data que o mesmo fez o cadastro no estabelecimento. Posteriomente, criou-se um histograma para visualizar a distribuição destes dados ao longo do tempo. Feito isto, foi criada a planilha dinâmica contendo os dados de ano/mês de entrada dos clientes, e no cabeçalho as semanas que se passaram desde o cadastro de entrada, com a contagem (em %) por cliente. Após, se fez a formatação condicional, diferenciando por cores os percentuais de retenção, com os mais escuros sendo os maiores percentuais, reduzindo a cor com a diminuição da retenção.
</details>

<details>
<summary><strong style="font-size: 16px;">Resultados e Conclusões</strong></summary>
Como resultado, foi possível observar que claramente este estabelecimento está com dificuldade de realizar a retenção dos clientes, uma vez que após o primeiro mês de cadastro do cliente, sua retenção já cai pela metade em quase todos os meses. No entanto, há alguns meses onde há uma maior retenção de clientes, como junho/2022, outubro/2021 e maio/2022. No mês de julho/2020, também a valores consideráveis de retenção, porém esta não é contínua, tendo meses onde não foi realizada nenhuma compra. Estas informações são importante pois podem auxiliar a equipe de marketing a elaborar estratégias de venda importantes para estes grupos. 
Somado a isso, também foi possível observar que os últimos meses deste banco de dados houve queda nas transações e nos cadastros, principalmente quando observamos ano a ano, onde a média de transações passou de 10,92 em 2020 para 8,72 em 2022. Além disso, há cadastro de entrada de clientes até o mês de junho/2022, porém existem transações sendo feitas até dezembro/2022, ou seja, não se está angariando clientes novos.  
Já observando as categorias de segmentação, foi possível identificar que as categorias “Campeões”, “Cliente Leal”, “Risco de Perda” e “Não posso perdê-lo” tem e melhor média de gasto neste estabelecimento, então seria bom focar em estratégias para estes grupos para priorizá-los.
</details>

