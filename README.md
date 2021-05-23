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

Base de Dados | Endereço na Web | Resumo descritivo
----- | ----- | -----
Índice de isolamento social | https://www.saopaulo.sp.gov.br/planosp/simi/dados-abertos/ | O índice de isolamento um índice atualizado diariamente com dados disponibilizados pelas prestadoras de serviços de telecomunicação e gerida pela Associação Brasileira de Recursos em Telecomunicações.

Os dados são Município1, Código Município IBGE, População estimada (2020), UF1, Data, Média de índice de Isolamento. O índice de isolamento é baseada na localização obtida pelas antenas de celulares que são marcadas como uma referência para o lugar onde o celular permaneceu entre as 22h00 e 2h00. Durante o dia, caso o celular tenha se afastado deste ponto de referência é definida como fora do isolamento. A distância percorrida para ser considerado como fora do isolamento é variável. Na cidade de São Paulo chega a aproximadamente 200 metros.
A maior dificuldade para utilizar estes dados foram que a data é constituída pelo dia da semana e a data sem o ano. Portanto foi necessário separar as duas informações e para converter para o formato datahora do python foi necessário adicionar o ano. Ao analisar os dados, percebemos que as informações são adicionadas do mais recente ao mais antigo e o dia da semana confirma qual o ano, portanto conseguimos adicionar o ano para as datas. Algumas datas estavam faltando, portanto completamos utilizando a média entre o dia anterior e o dia seguinte.

Base de Dados | Endereço na Web | Resumo descritivo
----- | ----- | -----
COVID-19 Community Mobility Reports | https://www.google.com/covid19/mobility/?hl=en | Estes dadis oferecem tem como objetivo oferecer ideias sobre o que mudou em resposta a políticas de combate a COVID-19. O relatório mostra a tendência de movimentação pelo tempo e geografia em diferentes categorias de locais como varejo e lazer, mercados e farmácias, parques, estações de transportes públicos, locais de trabalho e áreas residenciais

Os dados são country_region_code,country_region,sub_region_1,sub_region_2,metro_area,iso_3166_2_code,census_fips_code,place_id,date,retail_and_recreation_percent_change_from_baseline,grocery_and_pharmacy_percent_change_from_baseline,parks_percent_change_from_baseline,transit_stations_percent_change_from_baseline,workplaces_percent_change_from_baseline,residential_percent_change_from_baseline.


# Metodologia
Análise de séries temporais, análise dos componentes, redes neurais com LSTM.

# Ferramentas
Python – Linguagem de programação para processamento dos dados, análise dos componentes e projeções.

Jupyter Notebook - Aplicação Web para um ambiente de programação interativo e de fácil visualização.

Google Colab - Ambiente de programação hospedado na nuvem para processamento e compartilhamento.

Power Bi- cruzamento de bases de dados para obtenção de informações (demográficas, projeções, ...).


# Cronograma
![alt text](https://github.com/eitiyamamoto/MO826-projeto/blob/master/image/cronograma.png)
