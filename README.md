# Projeto O PERFIL DA MOBILIDADE URBANA NA CIDADE DE CAMPINAS/SÃO PAULO DURANTE A PANDEMIA DO SARS-CoV-2
# Project `THE PROFILE OF URBAN MOBILITY IN THE CITY OF CAMPINAS / SÃO PAULO DURING THE SARS- COV-2 PANDEMIC`

# Apresentação

O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação [*Ciência e Visualização de Dados em Saúde*](https://github.com/datasci4health/home), oferecida no primeiro semestre de 2021, na Unicamp.


> |Nome  | RA | Especialização|
> |--|--|--|
> | ANDERSON MAURICIO DE OLIVEIRA  | 264408  | Saúde|
> | DIEGO HENRIQUE DA SILVA  | 231381  | Saúde|
> | VICTOR EITI YAMAMOTO  | 157465  | Computação|
> | ANA PAULA DE OLIVEIRA DIAS  | 231273  | Saúde |
> | VANESSA GOMES LIMA  | 223810  | Saúde |


# Descrição Resumida do Projeto
A COVID-19, tem apresentado uma  taxa de letalidade de 2,8%, ceifando até o momento 428.034 vidas no Brasil³. Diante da disseminação rápida da doença, foi necessário adotar medidas de prevenção e mitigação, para isso, a OMS e o Ministério da Saúde no Brasil redigiram medidas de distanciamento social a serem seguidas como estratégia de controle da mobilidade da população, redução das atividades comerciais não essenciais, restrição de circulação de pessoas em eventos e transportes públicos, fechamento de escolas e universidades4. Além do uso obrigatório de máscaras,  dada a forma de contaminação via aerossóis e gotículas da COVID-19.

Logo, entre as medidas de prevenção do contágio e disseminação da COVID-19 estão o isolamento, o distanciamento social e o lockdown, ambos diretamente relacionados à mobilidade urbana, que é o foco do nosso trabalho. A mobilidade urbana pode ser definida definida como “o deslocamento das pessoas e bens na cidade, com objetivo de desenvolver atividades econômicas e sociais no perímetro urbano das cidades, aglomerações e regiões metropolitanas”.  Ela tem sido submetida à análise e intervenção por parte das autoridades governamentais e sanitárias como um dos fatores que interferem na transmissão do SARS-CoV-2 em nível global e no surgimento de novas variantes do vírus, como aconteceu em Manaus. 

Porém, observa-se que no Brasil não houve uma ação coordenada, uma vez que cada estado e cada município adotou as medidas em um tempo e de uma forma. Isso se deve a postura adotada pelo presidente em exercício, Jair Messias Bolsonaro, que muitas vezes se colocou contra as medidas de isolamento e distanciamento social e criando um dualismo entre a economia e a vida.
    
Evidencia-se pouca mudança de mobilidade entre a população mais pobres, o que denota que esta população encontra-se mais vulnerável e sob o risco de contaminação, além disso, a percepção das pessoas quanto ao isolamento social, varia conforme a renda, escolaridade, idade e sexo6, o que impacta em sua adesão.
O município de Campinas é o terceiro maior de São Paulo e possui amplas atividades técnico científicas, constituindo em grande polo tecnológico educacional. Conforme o boletim epidemiológico nº 10, de abril de 2021, apresentou 81.941 de pessoas com COVID-19, taxa de incidência por cem mil habitantes de 6.715,7 com 3% de letalidade, conforme figura 1-Introdução.

<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/epidemiologia-brasil-sp-campinas.png" alt="train_perf_fig" height="160" width="480"/>
    <br>
    <em>Figura 1-Introdução: Epidemiologia da COVID-19 no Brasil, no Estado de São Paulo e nos municípios de São Paulo e Campinas 2020-2021</em>
</p>

Com o crescimento da renda média dos brasileiros, aumento dos veículos nas ruas e preferência por transportes individuais, o ir e vir nas cidades está cada vez mais caótico. No Brasil, historicamente, a migração dos trilhos para o asfalto foi resultado de uma política de Estado que priorizou o investimento na indústria automobilística. Assim, o bonde deu lugar a ônibus, carros e motocicletas, misturando o transporte público e o privado, movido a gasolina e óleo diesel. Hoje, há alguns desafios da mobilidade urbana que destacam-se: limitação do fluxo; aumento do índice de acidentes, tendo como consequência mutilações graves ou mortes; pequena oferta de alternativa de mobilidade para atender o excesso de passageiros que dependem de transportes públicos e a poluição do ambiente.

As consequências da COVID-19 vão além das vidas perdidas, acarretando problemas emocionais, desemprego, crise econômica, hospitais sobrecarregados além de suas capacidades, faltando produtos de saúde básicos para prestar assistência aos pacientes, além de agudizar as desigualdades sociais dos países, sobretudo, aqueles em desenvolvimento, como é o caso do Brasil.   

Com isso, objetivou-se com esse estudo avaliar o perfil dessa mobilidade urbana na cidade de Campinas/ São Paulo, durante a pandemia do SARS CoV-2.


Vídeo de explicação: https://www.canva.com/design/DAEai0jTvls/LHTyoEe1CfSxXs6tmvJ7cg/view?utm_content=DAEai0jTvls&utm_campaign=designshare&utm_medium=link&utm_source=recording_view

Vídeo de apresentação final: https://drive.google.com/file/d/1jkwoC0r6qd7LIhRM2zbAo3YamDzWiGby/view

# Perguntas de Pesquisa
Qual a característica da mobilidade urbana na cidade de Campinas/ São Paulo durante a pandemia?

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

# Análises Realizadas
Com o objetivo de fazer uma previsão da quantidade de óbitos na cidade de Campinas utilizamos técnicas que trabalham com séries temporais.
A primeira técnica foi Support Vector Regression (SVR) Segmentamos os dados obtidos para os últimos seis dias, a fim de prever o próximo dia. O resultado não conseguiu encontrar uma tendência, apesar de em algumomento elevar exponencialmente

Para o segundo teste usamos uma técnica de otimização, o Stochastic Gradient Descent (SGD) que ajusta classificadores lineares e regressores.  Esta abordagem permitiu treinar o modelo e gerou uma previsão do comportamento geral satisfatória apresentando variâncias imputadas à sazonalidade.

No terceiro teste utilizamos um regressor AdaBoost, um meta estimador que começa ajustando um regressor no conjunto de dados original e, em seguida, ajusta cópias adicionais do regressor no mesmo conjunto de dados, porém não conseguiu aprender as tendências de crescimento e nem predizer a partir dos dados.

A quarta técnica aplicada foi Neural network, um modelo de relacionamentos não lineares complexos entre a variável de resposta e seus preditores. Como é um modelo interativo, para fazermos a previsão um passo a frente usamos uma entrada histórica que permite gerar uma predição, esta pode ser usa para prever quantos passos forem necessários à frente, desse modo gerou-se um treinamento adequado a partir da aprendizagem com o conjunto de testes.

As limitações encontradas na predição da quantidade de obitos giram em torno da amostra, usamos um curto espaço de tempo para gerar os dados de predição.

# Resultados

A tabela 1 mostra os resultados de coeficiente de determinação (score) e o erro quadrático médio (MSE) para cada modelo para os dados de óbitos totais por dia na cidade de Campinas. Os dados utilizados para o teste e validação foram do dia 25 de fevereiro de 2020 até o dia 20 de abril de 2021. Os primeiros 294 dias foram utilizados como conjunto de treinamento e o restante 127 dias foram utilizados como conjunto de treinamento. As features utilizadas foram os dados de óbitos totais dos 6 dias anteriores. Este valor foi selecionado com base na autocorrelação dos dados de óbitos totais. O coeficiente de determinação e o erro quadrático médio foram calculados utilizando o conjunto de testes. Ao comparar os modelos, podemos observar que todos os modelos tiveram o erro quadrático médio melhor que os modelos basais, mas o melhor resultado foi obtido pelo SGD regressor.

Tabela 1: Tabela relacionando os modelos testado, o coeficiente de determinação (score) e o erro quadrático médio (MSE) para óbitos totais por dia

|Modelo  | Score | MSE |
|--|--|--|
| Holt Winter  |   | 212.943|
| ARIMA  |   | 197.627 |
| SVR  | 0,989  | 1.806 |
| SGD  | 0,994 | 974 |
| NN  | 0,973  | 4.462 |

A figura 13 mostra um gráfico de data e o valor de óbitos totais na cidade de campinas e o valor predito pelo modelo ARIMA que foi utilizado como basal. Em azul está o valor dos dados de conjunto de treinamento, em laranja está o conjunto de teste e em verde o valor predito pelo ARIMA. Podemos observar que o modelo conseguiu aprender a tendência de crescimento, mas não tem um resultado bom.

<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/arima-obitos.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 13: Conjunto de teste e validação com os valores predito pelo modelo ARIMA para óbitos totais</em>
</p>

A figura 14 mostra os dados reais e os dados preditos pelo modelo SGD para óbitos totais na cidade de campinas. Em azul está o valor real do conjunto de treinamento, em verde está o conjunto de teste, em laranja os valores preditos pelo modelo para o conjunto de treinamento e em vermelho o conjunto predito  pelo modelo para o conjunto de teste. Podemos observar que o modelo conseguiu prever o comportamento geral dos óbitos totais.

<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/sgd-obitos.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 14: Conjunto de teste e validação com os valores predito pelo modelo SGD para óbitos totais</em>
</p>

A tabela 2 mostra os resultados de coeficiente de determinação (score) e o erro quadrático médio (MSE) para cada modelo para os dados de óbitos novos por dia na cidade de Campinas. Decidimos realizar a análise dos óbitos novos por apresentar um comportamento mais complexo que o apresentado pelos óbitos totais. O período utilizado para o conjunto de testes e treinamento foram iguais ao da Tabela 1. As features utilizadas foram os 6 dias anteriores e os valores de seno e cosseno do dia em relação a semana e ao ano. O código python abaixo mostra como foi calculado. Ao comparar os modelos, podemos observar que todos foram melhores que o modelo basal, mas o melhor resultado foi obtido pelas redes neurais (NN). Também é possível observar que os três modelos analisados (SVR, SGD e NN) tiveram scores piores em relação ao modelo de óbitos totais.

~~~python
day = 24 * 60 * 60
week = 7 * day
year = 365.2425 * day
timestamp = campinas_isolamento_lagged.index.map(pd.Timestamp.timestamp)
campinas_isolamento_lagged['week_sin'] = np.sin(timestamp * (2 * np.pi / week))
campinas_isolamento_lagged['week_cos'] = np.cos(timestamp * (2 * np.pi / week))
campinas_isolamento_lagged['year_sin'] = np.sin(timestamp * (2 * np.pi / year))
campinas_isolamento_lagged['year_cos'] = np.cos(timestamp * (2 * np.pi / year))
~~~
Tabela 2: Tabela relacionando os modelos testado, o coeficiente de determinação (score) e o erro quadrático médio (MSE) para óbitos por dia

|Modelo  | Score | MSE |
|--|--|--|
| Holt Winter  |   | 182,46 |
| ARIMA  |   | 219,03 |
| SVR  | 0,167  | 120,95 |
| SGD  | 0,110 | 129,30 |
| NN  | 0,398  | 97,42 |

A figura 15 mostra o gráfico de óbitos novos para a cidade de Campinas para o conjunto real e o previsto pelo modelo. Em azul está o conjunto real, em laranja está os valores preditos pelo modelo para o conjunto de validação e em verde está os valores preditos pelo modelo para o conjunto de teste. Podemos observar que o modelo mostra um crescimento dos casos, mas não consegue mostrar o comportamento geral.

<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/hw-obitos-novos.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 15: Conjunto de teste e validação com os valores predito pelo modelo Holt Winter para óbitos novos</em>
</p>

A figura 16 mostra o gráfico de óbitos novos para a cidade de Campinas para o conjunto real e o previsto pelas redes neurais. Em azul está o conjunto de treinamento, em verde está o conjunto de teste, em laranja está os valores previstos pelo modelo para o conjunto de treinamento e em vermelho os valores previstos para o conjunto de teste. Podemos observar que o modelo conseguiu expressar o comportamento geral e os ciclos de alta e queda semanal. Também podemos observar que ainda há um erro entre o previsto e real para o conjunto de treinamento, mas consegue ter uma boa previsão para o conjunto de teste.

<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/nn-obitos-novos.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 16: Conjunto de teste e validação com os valores predito pela redes neurais para óbitos novos</em>
</p>

A tabela 3 mostra os resultados de coeficiente de determinação (score) e o erro quadrático médio (MSE) para cada modelo para os dados de óbitos novos por dia na cidade de Campinas. Neste caso, utilizamos o mesmo período para o conjunto de teste e treinamento, mas adicionamos as features de mobilidade para os 30 dias anteriores. Todos os modelos foram melhores que os modelos basais, mas os scores e os erros foram piores do que os modelos sem os dados de mobilidade. Observamos que especialmente nas redes neurais, o modelo chegava ao overffiting muito rapidamente, fazendo com que o conjunto de treinamento fosse aprendido rapidamente, mas tivesse um resultado muito baixo no conjunto de teste.

Tabela 3: Tabela relacionando os modelos testado, o coeficiente de determinação (score) e o erro quadrático médio (MSE) para óbitos por dia utilizando os dados de mobilidade

|Modelo  | Score | MSE |
|--|--|--|
| SVR  | -0,075  | 140,89 |
| SGD  | 0,008 | 131,20 |
| NN  | 0,060  | 123,90 |

A figura 17 mostra o gráfico de óbitos novos para a cidade de Campinas para o conjunto real e o previsto pelas redes neurais com os dados de mobilidade. Em azul está o conjunto de treinamento, em verde está o conjunto de teste, em laranja está os valores previstos pelo modelo para o conjunto de treinamento e em vermelho os valores previstos para o conjunto de teste. Podemos observar que não é mais possíbel observar os dados reais para o conjunto de treinamento, pois o modelo está prevendo quase com exatidão os valores reais. Ao observar o conjunto de teste, podemos observar que o comportamento geral é bom visualmente, mas tem um erro maior do que o modelo representado na figura 16 e teve um score muito abaixo dos anteriores.

<p align="center">
 <img src="https://github.com/eitiyamamoto/MO826-projeto/blob/master/reports/figures/nn-obitos-novos-mobility.png" alt="train_perf_fig" height="320" width="480"/>
    <br>
    <em>Figura 17: Conjunto de teste e validação com os valores predito pelas redes neurais para óbitos novos utilizando dados de mobilidade</em>
</p>

# Conclusão
 A característica da mobilidade urbana na cidade de Campinas-SP na pandemia da COVID-19 no período de 25 de fevereiro de 2020 a 20 de abril de 2021 encontrada na nossa pesquisa foi a seguinte:

Crescimento das taxas de óbito, seguido de um decréscimo e posterior aumento; 
A média de índice de isolamento teve aumento entre abril e maio e depois uma constante queda;
A mobilidade para varejo, recreação, parque teve uma queda entre março e abril e depois houve constante crescimento;
Boa previsibilidade utilizando para os óbitos totais e para óbitos novos utilizando os dados de óbito dos seis dias anteriores, porém ao adicionar os dados de mobilidade tivemos uma piora do modelo da previsibilidade. 


desde o início da pandemia em fevereiro/2020 tendeu a acompanhar a tendência e variabilidade da maioria dos outros municípios e estados do Brasil.  

Essa mobilidade relacionada à circulação de pessoas,bens e  serviços mostrou-se mais restrita e intensa no começo da transmissão da pandemia onde algo novo e o medo de adquirir a doença de certa maneira se apossaram da população.E também de acordo com os decretos de restrição impostos pelas autoridades governamentais e orientações sanitárias.Alguns fatos que ocorreram,marcaram a mobilidade urbana, e permanecem até hoje,fazendo parte do nosso cotidiano:

1- Houve diminuição nos deslocamentos,de maneira geral

2 - Menos veículos de transporte público estão circulando,como ônibus,trens,etc.

3- Maior adesão aos serviços de delivery,já que as pessoas ficaram mais em suas residências;

4 - Aumento do uso de bicicletas e veículos, para se evitar aglomeração nos transportes públicos.

5 - E mesmo com as medidas de isolamento social,grande parte da população continuou usando os transportes públicos para poder continuar trabalhando,porém em condições precárias e complicadas pois os mesmos circularam mais cheios.

A percepção das pessoas quanto ao isolamento social,varia conforme à renda,escolaridade,idade e sexo.Sendo a população mais pobre menos adepta à restrições de circulação devido entre outras coisas a necessidade de obtenção e manutenção da renda familiar.   
Em geral mulheres e idosos tiveram mais adesão às restrições quando comparado aos homens e jovens.A faixa etária de 30 à 49 anos  tomou menos medidas restritivas de contato físico,sendo o principal ponto influenciador para isso, o trabalho. 

Pesquisas mostraram que ¼ da população aderiu pouco ou não aderiu às medidas de distanciamento social,o que tem reflexo no aumento da transmissibilidade do vírus,já que o distanciamento social é considerado umas das medidas mais bem sucedidas para evitar a propagação da Covid-19.

Isso mostra que o controle da mobilidade urbana,redução das atividades não essenciais,restrição da circulação de pessoas em eventos e transportes públicos,são importantes na prevenção e diminuição da disseminação da Covid-19. 


# Trabalhos Futuros
Como trabalhos futuros podemos sugerir o estudo de modelos utilizando uma quantidade de maior de cidades para criar um modelo mais robusto, estudo com uma quantidade maior de features para a previsão e efetuar a previsão de óbitos para um período maior de dias.

# Referências
1 FREITAS, André Ricardo Ribas; NAPIMOGA, Marcelo; DONALISIO, Maria Rita. Análise da gravidade da Pandemia de COVID-19. Epidemiol. Serv. Saúde, Brasília, Abr. 2020. Disponível em: https://www.scielosp.org/article/ress/2020.v29n2/e2020119/. Acesso em 21 maio 2021.

2 WORLD HEALTH ORGANIZATION. Coronavirus disease (COVID-19). Disponível em: https://www.who.int/emergencies/diseases/novel-coronavirus-2019/question-and-answers-hub/q-a-detail/coronavirus-disease-covid-19#:~:text=symptoms. Acesso em  23 maio 2021.

3 BRASIL, Painel Coronavírus. Disponível em: https://covid.saude.gov.br/. Acesso em 12 maio 2021 às 23:54.

4 GALHARDI, Cláudia Pereira; FREIRE, Neyson Pinheiro; MINAYO, Maria Cecília de Souza; FAGUNDES, Maria Clara Marques. Fato ou Fake? Uma análise da desinformação frente à pandemia da COVID-19 no Brasil. Ciênc. saúde coletiva, Rio de Janeiro, v. 25, supl. 2, p. 4201-4210, Out. 2020. Disponível em : http://www.scielo.br/scielo.php?script=sci_arttext&pid=S1413-81232020006804201&lng=en&nrm=iso. Acesso em 13 maio 2021.  

5 Referência definição de mobilidade urbana

6 BEZERRA, Anselmo César Vasconcelos et al . Fatores associados ao comportamento da população durante o isolamento social na pandemia de COVID-19. Ciênc. saúde coletiva,  Rio de Janeiro ,  v. 25, supl. 1, p. 2411-2421,  jun.  2020 .   Disponível em <http://www.scielo.br/scielo.php?script=sci_arttext&pid=S1413-81232020006702411&lng=pt&nrm=iso>. acessos em  23  maio  2021.  Epub 05-Jun-2020.  https://doi.org/10.1590/1413-81232020256.1.10792020.

# Cronograma
![alt text](https://github.com/eitiyamamoto/MO826-projeto/blob/master/image/cronograma.png)
