# Projeto O IMPACTO DO ISOLAMENTO SOCIAL NA INCIDÊNCIA DO SARS COVID 2 NO ESTADO DE SÃO PAULO
# Project `THE IMPACT OF SOCIAL ISOLATION ON THE INCIDENCE OF SARS COVID 2 IN THE STATE OF SÃO PAULO`

# Apresentação

O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação [*Ciência e Visualização de Dados em Saúde*](https://github.com/datasci4health/home), oferecida no primeiro semestre de 2021, na Unicamp.


> |Nome  | RA | Especialização|
> |--|--|--|
> | ANDERSON MAURICIO DE OLIVEIRA  | 264408  | Saúde|
> | DIEGO HENRIQUE DA SILVA  | 231381  | Saúde|
> | VICTOR EITI YAMAMOTO  | 157465  | Computação|
> | LUCIANO LOPES SALGADO  | 224035  | Computação|
> | EMÍDIO ANTÔNIO DE ARAÚJO NETO  | 265885  | Saúde|


# Descrição Resumida do Projeto
O SARS-COV-2 teve seu início em dezembro de 2019 em Wuhan, na China. Em 20 de Janeiro de 2020, a ONU classificou o surto como emergência de Saúde Pública de âmbito internacional e, em 11 de março de 2020, como pandemia. Um vírus de alta transmissibilidade atingindo as pessoas de todos os recantos do mundo, com mais de 2 milhões de mortos e esses números subindo diariamente.

Tem sido motivo de preocupações por parte dos Cientistas, governantes do mundo, organizações e instituições de Saúde e da população mundial. As consequências que se arrastam na sociedade são visíveis como: mortes, problemas emocionais, desemprego, crise econômica, Hospitais sobrecarregados além de suas capacidades, faltando produtos de saúde básicos para prestar assistência aos pacientes. Indícios de um mundo que envelhece piorando.
        
Além de medidas de higienização das mãos, uso de máscaras, e outras. Os governos têm adotado o isolamento social como uma das medidas para conter o avanço da doença e por estarmos vivenciando esse cenário no nosso cotidiano, resolvemos aferir o impacto que as medidas de  isolamento tem na incidência da Covid-19, como tema de nosso projeto de pesquisa.

Vídeo de explicação: https://www.canva.com/design/DAEai0jTvls/LHTyoEe1CfSxXs6tmvJ7cg/view?utm_content=DAEai0jTvls&utm_campaign=designshare&utm_medium=link&utm_source=recording_view

# Perguntas de Pesquisa
O isolamento social reduz a incidência?

# Bases de Dados

## Bases Estudadas e Adotadas
Base de Dados | Endereço na Web | Resumo descritivo
----- | ----- | -----
Casos e óbitos por município e data | https://www.saopaulo.sp.gov.br/planosp/simi/dados-abertos/ | Registro de casos e óbitos por município e data de notificação no Estado de São Paulo. Estes dados são distribuídos como dados abertos pelo governo do estado de São Paulo e são atualizadas diariamente

Os dados contém nome do município, código ibge, dia, mês, datahora, casos, casos novos, casos_pc (Casos totais por 100 mil habitantes), casos_mm7d (Média móvel dos últimos 7 dias dos novos casos), óbitos, óbitos novos, obitos_pc (Óbitos totais por 100 mil habitantes), obitos_mm7d (média móvel dos últimos 7 dias dos novos óbitos), letalidade, nome_ra (Nome da Região Administrativa), cod_ra (Código da Região Administrativa), nome_drs (Nome do Dpto. Regional de Saúde), cod_drs (Código do Dpto. Regional da Saúde), população estimada, população com mais de 60 anos, área em km2, rótulo da legenda para mapa, código da legenda para mapa, latitude, longitude, semana epidemiológica, descrição, nome do municpio, código do município no IBGE (7 dígitos), dia, mes.

A figura 1 mostra a evolução dos óbitos na cidade de campinas no período de março de 2020 até abril de 2021.

<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/obito-plot.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 1: Óbitos novos por dia na cidade de Campinas</em>
</p>

A figura 2 mostra a autocorrelação para óbitos novos em Campinias. Este gráfico foi utilizado para verificar se os valores de óbitos podem ser expressados pelos valores prévios de óbito. O valor da autocorrelação variam de -1 a 1 e a região em azul representa a confiança no valor, portanto apenas os valores fora da faixa azul é considerado significativa. Ao analisar o gráfico, podemos observar que há uma autocorrelação significativa até o 14o dia. A autocorrelação parcial analisa se há uma correlação entre o óbito do dia com um ponto no passado. Neste caso podemos observar que os dados são significativos ate o 3o dia.
<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/parque-auto.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 2: Análise de Autocorrelação e Autocorrelação parcial para óbitos novos em Campinas</em>
</p>

A figura 3 mostra a decomposição do gráfico de óbitos novos em tendência, sazonalidade e resto. A tendência é calculada usando média móvel centrada, a sazonalidade descreve a flutuação causada por eventos relacionados ao tempo e o residual é o resto da série temporal removendo a tendência e o padrão sazonal. Ao analisar a sazonalidade podemos observar que a média de óbitos tem uma sazonalidade bem definida.

<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/obito-decomposition.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 3: Decomposição para óbitos novos em Campinas</em>
</p>

Base de Dados | Endereço na Web | Resumo descritivo
----- | ----- | -----
Índice de isolamento social | https://www.saopaulo.sp.gov.br/planosp/simi/dados-abertos/ | O índice de isolamento um índice atualizado diariamente com dados disponibilizados pelas prestadoras de serviços de telecomunicação e gerida pela Associação Brasileira de Recursos em Telecomunicações.

Os dados são Município1, Código Município IBGE, População estimada (2020), UF1, Data, Média de índice de Isolamento. O índice de isolamento é baseada na localização obtida pelas antenas de celulares que são marcadas como uma referência para o lugar onde o celular permaneceu entre as 22h00 e 2h00. Durante o dia, caso o celular tenha se afastado deste ponto de referência é definida como fora do isolamento. A distância percorrida para ser considerado como fora do isolamento é variável. Na cidade de São Paulo chega a aproximadamente 200 metros.

A maior dificuldade para utilizar estes dados foram que a data é constituída pelo dia da semana e a data sem o ano. Portanto foi necessário separar as duas informações e para converter para o formato datahora do python foi necessário adicionar o ano. Ao analisar os dados, percebemos que as informações são adicionadas do mais recente ao mais antigo e o dia da semana confirma qual o ano, portanto conseguimos adicionar o ano para as datas. Algumas datas estavam faltando, portanto completamos utilizando a média entre o dia anterior e o dia seguinte.

A Figura 4 descreve o comportamento de isolamento social na cidade de campinas entre março de 2020 e abril de 2021.

<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/isolamento-plot.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 4: Isolamento na cidade de Campinas</em>
</p>

A figura 5 mostra a autocorrelação para o isolamento na cidade de Campinas. Podemos observar que a autocorrelação é significativa até o 17o dia e para a autocorrelação particla é significativa até o 7o dia.
<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/isolamento-auto.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 5: Análise de Autocorrelação e Autocorrelação parcial para o isolamento em Campinas</em>
</p>

A figura 6 mostra a decomposição das informações de isolamento na cidade de Campinas. A tendência de isolamento teve um aumento na em março, mas para o período subsequente teve uma constante queda na taxa de isolamento. A sazonalidade é bem definida com um pico curto e período de baixa.
<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/isolamento-decomposition.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 6: Decomposição do isolamento em Campinas</em>
</p>

Base de Dados | Endereço na Web | Resumo descritivo
----- | ----- | -----
COVID-19 Community Mobility Reports | https://www.google.com/covid19/mobility/?hl=en | Estes dadis oferecem tem como objetivo oferecer ideias sobre o que mudou em resposta a políticas de combate a COVID-19. O relatório mostra a tendência de movimentação pelo tempo e geografia em diferentes categorias de locais como varejo e lazer, mercados e farmácias, parques, estações de transportes públicos, locais de trabalho e áreas residenciais

Os dados são country_region_code,country_region,sub_region_1,sub_region_2,metro_area,iso_3166_2_code,census_fips_code,place_id,date,retail_and_recreation_percent_change_from_baseline,grocery_and_pharmacy_percent_change_from_baseline,parks_percent_change_from_baseline,transit_stations_percent_change_from_baseline,workplaces_percent_change_from_baseline,residential_percent_change_from_baseline.

Os dados de varejo e recriação, mercados e farmácias, parques, transporte público e local de trabalho tem características gerais parecidas, portanto nesta análise só apresentaremos as informações de varejo e recriação. A figura 7 apresenta os dados de varejo e recriação para a cidade de campinas entre março de 2020 até dezembro de 2020.
<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/varejo-plot.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 7: Mobilidade para varejo e recriação na cidade de Campinas</em>
</p>

A Figura 8 mostra a autocorrelação para varejo e recriação na cidade de campinas. Podemos observar que a autocorrelação é significativa até o 18o dia e a autocorrelação parcial é significativa apenas para o dia 1.

<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/varejo-auto.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 8: Autocorrelação para varejo e recriação na cidade de Campinas</em>
</p>

A figura 9 mostra a decomposição dos dados de varejo e recriação para a cidade de Campinas. A tendência inicial é de queda em março, mas ele vai aumentando até de queda até o final de dezembro quando há uma queda. A saznalidade tem um pico inicial que vai decrescendo até um pico para baixo.
<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/varejo-decomposition.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 9: Decomposição para varejo e recriação na cidade de Campinas</em>
</p>


A figura 10 mostra os dados para mobilidade na residência da cidade de Campinas para o período de março de 2020 até dezembro de 2020.
<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/residencia-plot.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 10: Mobilidade para residência na cidade de Campinas</em>
</p>

A figura 11 mostra a autocorrelação para residência na cidade de Campinas. Podemos observar que a autocorrelação é significativa até o 15o dia e o pico está no 7o dia. A autocorrelação parcial é significativa apenas para o dia 1.
<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/residencia-auto.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 11: Autocorrelação para residência na cidade de Campinas</em>
</p>

A figura 12 mostra a decomposição dos dados de residência na cidade de Campinas. A tendência inicial foi de aumento em março e abril, mas tem uma tendência de queda até o final de dezembro, quando há um pequeno aumento. A sazonalidade é bem definida com um pico negativo.

<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/residencia-decomposition.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 12: Decomposição para residência na cidade de Campinas</em>
</p>

# Metodologia
Análise de séries temporais, análise dos componentes, redes neurais com LSTM.

# Ferramentas
Python – Linguagem de programação para processamento dos dados, análise dos componentes e projeções.

Jupyter Notebook - Aplicação Web para um ambiente de programação interativo e de fácil visualização.

Google Colab - Ambiente de programação hospedado na nuvem para processamento e compartilhamento.

Power Bi- cruzamento de bases de dados para obtenção de informações (demográficas, projeções, ...).


# Cronograma
![alt text](https://github.com/eitiyamamoto/MO826-projeto/blob/master/image/cronograma.png)
