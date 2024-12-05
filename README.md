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
<p> Este trabalho será desenvolvido com uma Análise Exploratória de Dados, utilizando o conjunto de dados previamente selecionado. A entrega final será um relatório detalhado, realizada pelo grupo. O link do repositório no GitHub, contendo o relatório e o código-fonte, deverá ser enviado por e-mail. Além dos scripts, recomenda-se a edição do arquivo README no GitHub para a adequada apresentação dos resultados obtidos.
</p>

#

<b>Introdução:</b><br>
O relatório documenta a análise exploratória realizada sobre o conjuntode dados "Learning Poverty (Pobreza de Aprendizagem)". O objetivo desta análise é avaliar a qualidade dos dados, suas características principais e identificar a presença de outliers, além de explorar as correlações entre as variáveis. 
<br>

<b>Contextualização da base de dados:</b><br>
Learning Poverty (Pobreza de Aprendizagem), desenvolvido pelo Banco Mundial, que mede a incapacidade de uma criança de 10 anos em ler e compreender um texto simples. Este indicador combina duas variáveis principais: a proporção de crianças que não atingem a proficiência mínima em leitura, medida diretamente nas escolas, e a porcentagem de crianças fora da escola, com a presunção de que essas crianças não possuem essa proficiência.
A base de dados inclui informações de diversos países e anos, fornecendo uma visão detalhada das desigualdades no aprendizado infantil ao redor do mundo. Dados sobre a proficiência de leitura de crianças por gênero, a porcentagem de crianças fora da escola e indicadores de aprendizado geral, segmentados por regiões geográficas e metodologias específicas, como as do GAML (Global Alliance to Monitor Learning).
Esses dados oferecem uma perspectiva global sobre a situação educacional, evidenciando as variações significativas entre diferentes regiões e destacando a necessidade de políticas educacionais eficazes que não apenas garantam o acesso à escola, mas também assegurem que as crianças realmente adquiram as habilidades essenciais de leitura e compreensão.
<br>
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
Aos valores ausentes, a análise inicial revelou que algumas colunas apresentavam uma quantidade significativa de dados faltantes. Para tratar isso, foi adotada a estratégia de substituir os valores ausentes nas variáveis numéricas pela mediana de cada coluna. Isso foi feito para evitar que valores extremos ou outliers influenciassem negativamente o processo de imputação. A escolha da mediana, em vez da média, se deu por ser uma abordagem mais robusta frente à presença de valores atípicos. Ao preenchimento dos valores ausentes, a integridade dos dados foi restaurada, permitindo uma análise mais precisa e confiável nas etapas subsequentes.
<br>

Identificação de Outliers:<br>
Para a identificação de possíveis outliers, foram gerados boxplots das variáveis numéricas. Essas visualizações permitiram uma análise gráfica da distribuição dos dados, facilitando a identificação de pontos que se afastam significativamente dos quartis. A identificação de outliers é uma etapa crítica para compreender a variação nos dados e seu potencial impacto nas análises subsequentes.
<br>

![image](https://github.com/user-attachments/assets/7e0d70b4-e985-42eb-b6f8-3078bb622fd2)


<br>
<b>children_reading_proficiency (proficiência de leitura das crianças:</b> A variável geral de proficiência em leitura de crianças apresenta uma distribuição relativamente ampla, com um intervalo interquartil que varia de aproximadamente 20 a 60. Não há muitos outliers identificados, sugerindo que a maior parte dos dados está dentro do intervalo esperado.
<br>

<b>female_children_reading_proficiency (proficiência de leitura entre meninas):</b> A distribuição da proficiência de leitura entre meninas apresenta uma mediana inferior à variável geral, por volta de 20, e um número considerável de outliers. Isso sugere uma concentração de dados mais baixos, com algumas observações que se afastam dos quartis superiores.
<br>

<b>male_children_reading_proficiency (proficiência de leitura entre meninos):</b> A distribuição da proficiência de leitura entre meninos é semelhante à das meninas, com uma mediana um pouco maior (aproximadamente 30) e uma concentração de dados dentro dos quartis. Também há outliers, mas em menor número comparado à variável das meninas.
<br>

<b>children_out_of_school (crianças fora da escola):</b> Esta variável, relacionada ao número de crianças fora da escola, tem uma mediana muito baixa (próxima de zero), indicando que, na maior parte das amostras, poucas crianças estão fora da escola. No entanto, há muitos outliers, o que pode indicar localidades ou situações excepcionais em que há um número significativamente maior de crianças fora da escola.
<br>

<b>female_children_out_of_school (meninas fora da escola):</b> A distribuição de meninas fora da escola segue um padrão semelhante à variável geral, com uma mediana próxima de zero e uma quantidade expressiva de outliers. Isso pode refletir contextos em que a exclusão escolar feminina é mais acentuada em certas regiões ou grupos.
<br>

<b>male_children_out_of_school (meninos fora da escola):</b> De forma semelhante às outras variáveis de exclusão escolar, a mediana está próxima de zero, com muitos outliers. A distribuição é comparável à das meninas, o que sugere que, em geral, há padrões semelhantes de exclusão escolar entre os gêneros, com exceções em alguns casos específicos.
<br>
<br>
conclusão de Outliers:<br>
Embora a maioria dos países tenha alcançado progressos consideráveis em áreas como proficiência de leitura e acesso escolar, as desigualdade ainda são evidentes e exigem atenção contínua. Em termos de proficiência de leitura, embora a maioria das crianças esteja dentro de um intervalo esperado, há variações regionais que podem refletir desigualdades no acesso à educação de qualidade. Além disso, as desigualdade de gênero são notáveis, com as meninas, em média, apresentando um desempenho inferior ao dos meninos em várias regiões, o que pode ser reflexo de fatores sociais e culturais que limitam as oportunidades de aprendizado para as meninas.
<br>
<br>
Análise de Correlação:<br>
Por fim, foi realizada uma análise de correlação entre as variáveis numéricas, resultando na construção de uma matriz de correlação. Essa análise é fundamental para entender as inter-relações entre as variáveis, fornecendo insights valiosos para investigações futuras. A matriz foi visualizada através de um heatmap, que evidenciou tanto correlações positivas quanto negativas.
<br>

Contextualização de Correlação:<br>
Há uma correlação negativa entre a proficiência de leitura (tanto geral quanto por gênero) e a porcentagem de crianças fora da escola. Isso faz sentido, pois países com menores taxas de exclusão escolar tendem a ter melhores índices de proficiência em leitura, indicando que a escolarização é um fator importante para a melhoria das habilidades de leitura.<br>
As correlações entre as variáveis de proficiência de leitura entre meninos e meninas também são visíveis, o que sugere que os padrões de aprendizado entre os gêneros estão relacionados, embora existam disparidades em alguns casos.

![image](https://github.com/user-attachments/assets/ddeb4195-9641-44b6-9719-3118cc7dc427)


<br>

<b>Escolha Adequada de Técnicas Estatísticas:</b><br>
Neste trabalho, utilizamos as bibliotecas pandas, seaborn e matplotlib para realizar uma análise exploratória dos dados. Cada uma dessas ferramentas desempenhou um papel essencial na manipulação, visualização e análise dos dados.

Primeiramente, a biblioteca pandas foi utilizada para carregar o conjunto de dados com o comando pd.read_csv(). Isso nos permitiu importar as informações e visualizar as primeiras linhas, o que foi importante para entender a estrutura dos dados e o tipo de variáveis com que estávamos lidando. Além disso, o pandas foi fundamental para identificar e calcular a quantidade de valores ausentes em cada coluna. O comando isnull().sum() nos ajudou a detectar quais variáveis tinham valores faltantes, e então calculamos o percentual de valores ausentes com base no tamanho do conjunto de dados. Em seguida, realizamos o tratamento dos valores ausentes utilizando a função fillna() do pandas, substituindo os valores faltantes nas variáveis numéricas pela mediana de cada coluna. Isso foi feito para evitar que valores extremos (outliers) distorcessem os resultados, garantindo uma imputação mais representativa.

Na fase de visualização, utilizamos a biblioteca seaborn para criar um boxplot, que é uma ferramenta visual útil para identificar outliers. O gráfico foi gerado para as variáveis numéricas mais relevantes, como children_reading_proficiency e children_out_of_school, o que permitiu identificar possíveis outliers nas distribuições dessas variáveis. Isso ajudou a garantir que a análise subsequente considerasse as irregularidades de maneira adequada. Além disso, usamos seaborn para gerar um heatmap da matriz de correlação entre as variáveis numéricas. Esse gráfico nos permitiu visualizar as relações entre diferentes variáveis, indicando como elas estão correlacionadas. Essa matriz de correlação é fundamental para identificar padrões de comportamento entre as variáveis, como a relação entre a proficiência de leitura e a porcentagem de crianças fora da escola, fornecendo insights valiosos para a análise.

Por fim, a função describe() do pandas foi aplicada para gerar estatísticas descritivas das variáveis numéricas, como média, mediana, mínimo, máximo e desvio padrão. Esse passo foi essencial para resumir as principais características dos dados e verificar a presença de outliers ou distribuições inusitados. As estatísticas descritivas também fornecem uma visão geral dos valores centrais e da dispersão dos dados, o que é crucial para entender a variabilidade nas variáveis estudadas.

Combinando essas ferramentas de análise de dados, conseguimos realizar uma análise exploratória, identificando e tratando problemas de qualidade dos dados (como valores ausentes e outliers), além de visualizar relações importantes entre as variáveis. Isso nos permitiu extrair insights valiosos sobre o conjunto de dados, atendendo aos critérios estabelecidos para a análise exploratória.

<b>Conclusão:</b><br>
A análise exploratória de dados proporcionou uma compreensão abrangente do conjunto de dados "Learning Poverty". Através da identificação e tratamento de valores ausentes, da visualização das distribuições das variáveis por meio de boxplots e da análise das correlações, foi possível identificar padrões e exceção importantes que ajudam a entender as desigualdades educacionais globais.<br>
Embora existam países com boas taxas de escolarização e proficiência de leitura, ainda há muitos desafios, especialmente em regiões com altos índices de crianças fora da escola e variações significativas no aprendizado entre meninos e meninas. A presença de outliers, especialmente em variáveis como "crianças fora da escola", destaca a necessidade de uma análise mais profunda em países ou regiões específicas.

links:<br>
Google Colab: https://colab.research.google.com/drive/1GCH7um-yeTxzlsf0JQvV-gYgF8sQqfUq?usp=sharing <br>
Banco de dados: https://basedosdados.org/dataset/e9493734-a30d-4f2b-9d88-8c8a6a217ce2?table=941dd793-fa77-439e-ba7f-3449c7a781d0
