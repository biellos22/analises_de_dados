<h1 align="center"> Trabalho de Probabilidade e Estatística</h1>
<img src="https://universidadedevassouras.edu.br/wp-content/uploads/2021/12/logo_horizontal_univasso.svg">

<h5>Curso: Engenharia de Software<br>
Disciplica: Probabilidade e Estatística<br>
Professor: Rafael Mynssem Brum<br>
Período: 6° Período<br>
Aluno: Gabriel Victor Martins Carvalho - Turma B<br>
ㅤㅤㅤ Davi Costa Antunes Narcizo - Turma B<br>
ㅤㅤㅤ Caio Cezar Jotta Nogueira - Turma B<br>
ㅤㅤㅤ Yago da Costa Jardim Alves Braga - Turma B<br>
ㅤㅤㅤ Daniel Monteiro de Carvalho - Turma B


</h5>

<h6 align="center">Descrição breve</h6>
<p>O trabalho a seguir deverá ser desenvolvido por meio de uma Análise Exploratória de Dados, utilizando o conjunto de dados previamente selecionado. A entrega final consistirá em um relatório detalhado da análise realizada pelo grupo. O link do repositório no GitHub, contendo o relatório e o código-fonte, deverá ser enviado por e-mail. Além dos scripts, recomenda-se a edição do arquivo README no GitHub para a adequada apresentação dos resultados obtidos.
</p>

#

<b>Introdução:</b><br>
O presente relatório documenta a exploração de dados realizada sobre o conjunto de dados intitulado "Learning Poverty (Pobreza de Aprendizagem)". O objetivo desta análise é compreender a qualidade dos dados, suas características principais e identificar a presença de outliers, além de examinar as correlações entre as variáveis. 
<br>

Carregamento e Visualização Inicial:<br>
O processo de exploração foi iniciado com o carregamento do arquivo CSV, seguido pela exibição das primeiras linhas do conjunto de dados. Esta etapa inicial foi crucial para uma familiarização com as variáveis presentes, permitindo uma primeira visão sobre a estrutura e os tipos de dados disponíveis.
<br>

Verificação de Valores Ausentes:<br>
Uma análise detalhada foi conduzida para identificar valores ausentes em cada coluna do DataFrame. Foi calculada a quantidade total e o percentual de valores ausentes, apresentados em um DataFrame específico. Esta análise revelou a extensão dos dados incompletos, evidenciando a necessidade de estratégias adequadas para tratamento, de forma a assegurar a robustez das análises futuras.
<br>

Estatísticas Descritivas:<br>
Foram calculadas as estatísticas descritivas para as variáveis numéricas. Este cálculo incluiu medidas como média, mediana, desvio padrão, valores mínimo e máximo, entre outros. As estatísticas descritivas proporcionaram uma compreensão aprofundada da distribuição e variabilidade dos dados, facilitando a identificação de padrões e anomalias.
<br>

Tratamento de Valores Ausentes:<br>
Optou-se por preencher os valores ausentes nas colunas numéricas utilizando a mediana, uma abordagem que se mostra robusta em relação à presença de outliers. Para garantir a integridade dos dados, foi criada uma cópia do DataFrame original antes da aplicação da mediana. Este tratamento é essencial para preparar os dados para análises estatísticas mais avançadas.
<br>

Identificação de Outliers:<br>
Para a identificação de possíveis outliers, foram gerados boxplots das variáveis numéricas. Essas visualizações permitiram uma análise gráfica da distribuição dos dados, facilitando a identificação de pontos que se afastam significativamente dos quartis. A identificação de outliers é uma etapa crítica para compreender a variação nos dados e seu potencial impacto nas análises subsequentes.
<br>

![download](https://github.com/user-attachments/assets/919b8a30-797d-411c-b87d-f88f3f50f115)

Com base no gráfico acima está uma análise dos dados presentes na imagem;<br>
<br>

<b>children_reading_proficiency:</b> A variável geral de proficiência em leitura de crianças apresenta uma distribuição relativamente ampla, com um intervalo interquartil que varia de aproximadamente 20 a 60. Não há muitos outliers identificados, sugerindo que a maior parte dos dados está dentro do intervalo esperado.
<br>

<b>female_children_reading_proficiency:</b> A distribuição da proficiência de leitura entre meninas apresenta uma mediana inferior à variável geral, por volta de 20, e um número considerável de outliers. Isso sugere uma concentração de dados mais baixos, com algumas observações que se afastam dos quartis superiores.
<br>

<b>male_children_reading_proficiency:</b> A distribuição da proficiência de leitura entre meninos é semelhante à das meninas, com uma mediana um pouco maior (aproximadamente 30) e uma concentração de dados dentro dos quartis. Também há outliers, mas em menor número comparado à variável das meninas.
<br>

<b>children_out_of_school:</b> Esta variável, relacionada ao número de crianças fora da escola, tem uma mediana muito baixa (próxima de zero), indicando que, na maior parte das amostras, poucas crianças estão fora da escola. No entanto, há muitos outliers, o que pode indicar localidades ou situações excepcionais em que há um número significativamente maior de crianças fora da escola.
<br>

<b>female_children_out_of_school:</b> A distribuição de meninas fora da escola segue um padrão semelhante à variável geral, com uma mediana próxima de zero e uma quantidade expressiva de outliers. Isso pode refletir contextos em que a exclusão escolar feminina é mais acentuada em certas regiões ou grupos.
<br>

<b>male_children_out_of_school:</b> De forma semelhante às outras variáveis de exclusão escolar, a mediana está próxima de zero, com muitos outliers. A distribuição é comparável à das meninas, o que sugere que, em geral, há padrões semelhantes de exclusão escolar entre os gêneros, com exceções em alguns casos específicos.
<br>


Análise de Correlação:<br>
Por fim, foi realizada uma análise de correlação entre as variáveis numéricas, resultando na construção de uma matriz de correlação. Essa análise é fundamental para entender as inter-relações entre as variáveis, fornecendo insights valiosos para investigações futuras. A matriz foi visualizada através de um heatmap, que evidenciou tanto correlações positivas quanto negativas.
<br>

![download (1)](https://github.com/user-attachments/assets/c3d2470d-e634-4403-8156-7b33613df3ee)

<br>

<b>Escolha Adequada de Técnicas Estatísticas:</b><br>
Neste trabalho, utilizamos as bibliotecas pandas, seaborn e matplotlib para realizar uma análise exploratória dos dados. Cada uma dessas ferramentas desempenhou um papel essencial na manipulação, visualização e análise dos dados.

Primeiramente, a biblioteca pandas foi utilizada para carregar o conjunto de dados com o comando pd.read_csv(). Isso nos permitiu importar as informações e visualizar as primeiras linhas, o que foi importante para entender a estrutura dos dados e o tipo de variáveis com que estávamos lidando. Além disso, o pandas foi fundamental para identificar e calcular a quantidade de valores ausentes em cada coluna. O comando isnull().sum() nos ajudou a detectar quais variáveis tinham valores faltantes, e então calculamos o percentual de valores ausentes com base no tamanho do conjunto de dados. Em seguida, realizamos o tratamento dos valores ausentes utilizando a função fillna() do pandas, substituindo os valores faltantes nas variáveis numéricas pela mediana de cada coluna. Isso foi feito para evitar que valores extremos (outliers) distorcessem os resultados, garantindo uma imputação mais representativa.

Na fase de visualização, utilizamos a biblioteca seaborn para criar um boxplot, que é uma ferramenta visual útil para identificar outliers. O gráfico foi gerado para as variáveis numéricas mais relevantes, como children_reading_proficiency e children_out_of_school, o que permitiu identificar possíveis valores inusitados nas distribuições dessas variáveis. Isso ajudou a garantir que a análise subsequente considerasse as irregularidade de maneira adequada. Além disso, usamos seaborn para gerar um heatmap da matriz de correlação entre as variáveis numéricas. Esse gráfico nos permitiu visualizar as relações entre diferentes variáveis, indicando como elas estão correlacionadas. Essa matriz de correlação é fundamental para identificar padrões de comportamento entre as variáveis, como a relação entre a proficiência de leitura e a porcentagem de crianças fora da escola, fornecendo insights valiosos para a análise.

Por fim, a função describe() do pandas foi aplicada para gerar estatísticas descritivas das variáveis numéricas, como média, mediana, mínimo, máximo e desvio padrão. Esse passo foi essencial para resumir as principais características dos dados e verificar a presença de outliers ou distribuições inusitados. As estatísticas descritivas também fornecem uma visão geral dos valores centrais e da dispersão dos dados, o que é crucial para entender a variabilidade nas variáveis estudadas.

Combinando essas ferramentas de análise de dados, conseguimos realizar uma análise exploratória, identificando e tratando problemas de qualidade dos dados (como valores ausentes e outliers), além de visualizar relações importantes entre as variáveis. Isso nos permitiu extrair insights valiosos sobre o conjunto de dados, atendendo aos critérios estabelecidos para a análise exploratória.

<b>Conclusão:</b><br>
A exploração de dados conduzida neste estudo forneceu uma base sólida para a compreensão da qualidade e estrutura do conjunto de dados. As etapas realizadas, que incluíram a identificação e o tratamento de valores ausentes, a análise de outliers e a exploração das correlações entre variáveis.

links:<br>
Google Colab: https://colab.research.google.com/drive/1GCH7um-yeTxzlsf0JQvV-gYgF8sQqfUq?usp=sharing <br>
Banco de dados: https://basedosdados.org/dataset/e9493734-a30d-4f2b-9d88-8c8a6a217ce2?table=941dd793-fa77-439e-ba7f-3449c7a781d0
