# 💰 Análise do mercado de crypto 💰

## 📋 Recolha de dados e API's usados📋
Os dados foram recolhidos através das API's fornecidas dos websites [Coingecko](https://www.coingecko.com/pt) e [Yahoo! Finance](https://finance.yahoo.com/) onde foram feitos “requests” de dados sobre o preço, volume e "market cap" de diversas cryptomoedas. Foram feitos mais "requests" de dados históricos das moedas Bitcoin, Ethereum e Cardano. Para o caso do Bitcoin a base de dados pedida foi entre 2013-04-28 até 2021. Já no caso do Ethereum, por ser uma moeda mais recente, a base de dados pedida apenas abrange dados entre 2015-08-07 até 2021. E para o Cardano, como a moeda mais recente destas 3, abrange desde 2017-10-18 até 2021. Todos foram fornecidos através do formato .json.

A Coingecko é uma plataforma que fornece uma análise fundamental do mercado de criptomoedas. Além de acompanhar preços, volume e capitalização de mercado, a CoinGecko acompanha o crescimento da comunidade, desenvolvimento do código-fonte aberto, principais eventos e métricas em cadeia.

Os csv's foram criados com os dataframes fornecidos pelas API's com o Jupyter Notebook.

Yahoo! Finance é uma propriedade de mídia que faz parte do Yahoo! rede de Ele fornece notícias financeiras, dados e comentários, incluindo cotações de ações, press releases, relatórios financeiros e conteúdo original. Ele também oferece algumas ferramentas online para gerenciamento de finanças pessoais.

Limpámos alguns dados que não eram relevantes para este projeto de forma a conseguirmos uma base de dados mais limpa e fácil de trabalhar no nosso objetivo.

Existe um dado, proveniente da base de dados fornecida pela Coingecko, por volta de 2017 na coluna de "Market Cap" que está alterado com o dado do dia seguinte por nao existir qualquer dado para aquele dia em relação ao "market cap". Para contornar este problema decidimos encontrar o index do dia em que se encontra o erro nos dados e substituir por 0.

Convertemos o tempo epoch em tempo ISO 8601 para ser percetível a qualquer humano ler a data.

## 🤔 Contexto 🤔 
Com o crescente interesse em criptoativos, durante o ano de 2020, decidimos realizar o nosso trabalho de forma a explorar alguns dados estatisticos relacionados com o tema.
A maioria dos sites que faz o reportório deste tipo de dados disponibiliza-os de uma forma geral e oferece pouca organização destas informações, desta forma também ficam mais facilmente inspeccionáveis/manipuláveis. Sem este tipo de trabalho tornam-se dificultadas as tarefas de análise, modelação e visualização por parte da comunidade de criptomoedas.

Como as API estão disponiveis na nuvem destes websites, então não é necessário descarregar-las e fica fácil para qualquer utilizador que quiser aceder a estes dados relativamente aos seus investimentos nesta área a partir do github.

A estrutura base deste ficheiro, desenhada para fácil manipulação em Excel/Python/R, não mudará, podendo a comunidade analítica considerá-lo um alvo imutável (em termos de localização e estrutura) para, por exemplo, alimentar plataformas de visualização/modelação. De notar que, mediante no final do ano 2021 com os relatórios da situação que irão decorrer, poderão ser adicionadas novas colunas desde que fornecidas pelo mesmo website e tratadas da mesma forma, mantendo-se claro a retrocompatibilidade. Fontes adicionais de dados poderão também então ser adicionadas.

Este projeto pode ser considerado ético e público assim como todos os dados do sistema blockchain são públicos, não é necessário recorrer a qualquer dado considerado privado.

Porque todas as boas decisões começam com bons dados.

## 🧱 Estrutura 🧱
[Análise de mercado de cryptomoedas em relação a MarketShare](https://github.com/cdm2021/Analise_Mercado_Crypto/blob/main/Notebooks/Análise%20de%20mercado%20de%20cryptomoedas%20no%20geral.ipynb).

[Preço, Volume e ROI Anual, de 30, 60 e 90 dias do par BTC-USD](https://github.com/cdm2021/Analise_Mercado_Crypto/blob/main/Notebooks/Pre%C3%A7o%2C%20Volume%20e%20ROI%20Anual%20do%20par%20BTC-USD.ipynb).

[Preço, Volume e ROI Anual, de 30, 60 e 90 dias do par ETH-USD](https://github.com/cdm2021/Analise_Mercado_Crypto/blob/main/Notebooks/Pre%C3%A7o%2C%20Volume%20e%20ROI%20Anual%20do%20par%20ETH-USD.ipynb).

[Preço, Volume e ROI Anual, de 30, 60 e 90 dias do par ADA-USD](https://github.com/cdm2021/Analise_Mercado_Crypto/blob/main/Notebooks/Pre%C3%A7o%2C%20Volume%20e%20ROI%20Anual%20do%20par%20ADA-USD.ipynb).

[Volatilidade BTC_ETH_ADA Yahoo](https://github.com/cdm2021/Analise_Mercado_Crypto/blob/main/Notebooks/Volatilidade%20BTC_ETH_ADA%20Yahoo.ipynb).

[Efficient Frontier - Simulação Monte Carlo](https://github.com/cdm2021/Analise_Mercado_Crypto/blob/main/Notebooks/Efficient%20Frontier%20-%20Simula%C3%A7%C3%A3o%20Monte%20Carlo.ipynb).

## 🚀 Funções das aplicações 🚀
Aviso Legal: Este trabalho nao tem como intuito de dar aconcelhamento financeiro, tem apenas o intuito de verificar dados de ação de preço ao longo dos anos.

Análise de mercado de cryptomoedas em relação a MarketShare - Representação gráfica e atualizada de partilha de mercado entre as 100 maiores Criptomoedas em 2020. O uso de "others" serve para simplificar o gráfico e obter uma melhor visualização sobre as moedas que com maior valor total de mercado.

Preço, Volume e ROI Anual, de 30, 60 e 90 dias do par BTC-USD - Preço e Volume de negócio da Bitcoin histórico desde 28/04/2013 até 28/05/2021. O ROI foi calculado a partir do dia 1 de cada mês e acabando 30/60/90 dias depois. O cálculo e representação visual do ROI feito no nosso trabalho é uma ferramenta que pode ajudar em futuros investimentos, tendo em conta a ação de preço nos anos anteriores. 

Preço, Volume e ROI Anual, de 30, 60 e 90 dias do par ETH-USD - Preço e Volume de negócio da Ethereum histórico desde 07/08/2015 até 28/05/2021. O ROI foi calculado a partir do dia 1 de cada mês e acabando 30/60/90 dias depois. O cálculo e representação visual do ROI feito no nosso trabalho é uma ferramenta que pode ajudar em futuros investimentos, tendo em conta a ação de preço nos anos anteriores. 

Preço, Volume e ROI Anual, de 30, 60 e 90 dias do par ADA-USD - Preço e Volume de negócio do Cardano histórico desde 18/10/2017 até 28/05/2021. O ROI foi calculado a partir do dia 1 de cada mês e acabando 30/60/90 dias depois. O cálculo e representação visual do ROI feito no nosso trabalho é uma ferramenta que pode ajudar em futuros investimentos, tendo em conta a ação de preço nos anos anteriores.

Volatilidade BTC_ETH_ADA Yahoo - A Volatilidade pode ser vista como uma linha de média da mudança do preço. A volatilidade é uma boa representação visual do risco de uma moeda.

Efficient Frontier - Simulação Monte Carlo - A "Efficient Frontier" é uma ferramenta visual que toma em conta o "Sharpe Ratio" de um determinado portfólio. Neste caso apenas foi calculados portfólios com as moedas BTC e ETH por nao haver dados históricos suficientes da moeda ADA/Cardano. A Simulação Monte Carlo é qualquer simulação que para a obtenção dos resultados faça o uso de dados aleatórios. A Simulação Monte Carlo foi utilizada na criação de potenciais portfólios, assim podemos criar e testar a quantidade de portfólios que achar-mos necessários para as nossas conlusões.

## 📔 Dicionário dos dados 📔

YahooFinance_bitcoin_price_volume_20140916_20210528.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Date |  Data | DD-MM-YYYY h-m-s-ms |
|  High |  é o preço máximo durante um certo dia | >=0 |
|  Low |  é o preço mínimo durante um certo dia | >=0 |
|  Open |  é o preço da primeira trade do dia | >=0 |
|  Close |  é o preço da última trade do dia | >=0 |
| Volume |  Total de moedas trocadas num determinado período de tempo | >=0 |
| Adj Close |  corrige o preço de "Close" de uma trade para refletir o valor dessa ação após a contabilização de quaisquer ações corporativas | >=0 |

YahooFinance_cardano_price_volume_20170930_20210528.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Date |  Data | DD-MM-YYYY h-m-s-ms |
|  High |  é o preço máximo durante um certo dia | >=0 |
|  Low |  é o preço mínimo durante um certo dia | >=0 |
|  Open |  é o preço da primeira trade do dia | >=0 |
|  Close |  é o preço da última trade do dia | >=0 |
| Volume |  Total de moedas trocadas num determinado período de tempo | >=0 |
| Adj Close |  corrige o preço de "Close" de uma trade para refletir o valor dessa ação após a contabilização de quaisquer ações corporativas | >=0 |


YahooFinance_ethereum_price_volume_20150806_20210528.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Date |  Data | DD-MM-YYYY h-m-s-ms |
|  High |  é o preço máximo durante um certo dia | >=0 |
|  Low |  é o preço mínimo durante um certo dia | >=0 |
|  Open |  é o preço da primeira trade do dia | >=0 |
|  Close |  é o preço da última trade do dia | >=0 |
| Volume |  Total de moedas trocadas num determinado período de tempo | >=0 |
| Adj Close |  corrige o preço de "Close" de uma trade para refletir o valor dessa ação após a contabilização de quaisquer ações corporativas | >=0 |


bitcoin_price_marketcap_volume_20130428_20210528.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  data |  Data | DD-MM-YYYY h-m-s-ms |
|  BTCUSD |  Valor da Bitcoin em dólares | >=0 |
|  marketcap |  Valor total de mercado de uma moeda | >=0 |
|  volume |  Total de moedas trocadas num determinado período de tempo |  >=0  |


bitcoin_roi_30_dias_mensal_2014-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Ano |  Ano  |  YYYY  |
|  Meses |  Meses do Ano  | Mes |
|  ROI 30 Dias 2014 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2014  |0 <= x <= 100, com valor percentual   |
|  ROI 30 Dias 2015 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2015  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2016 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2016  | 0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2017 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2017  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2018 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2018  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2019 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2019  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2020 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2020  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias Médio |  Roi médio  |  0 <= x <= 100, com valor percentual  |

bitcoin_roi_60_dias_mensal_2014-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Meses |  Meses do Ano  | Mes |
|  ROI 60 Dias 2014 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2014  |  0 <= x <= 100, com valor percentual |
|  ROI 60 Dias 2015 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2015  |  0 <= x <= 100, com valor percentual  |
|  ROI 60 Dias 2016 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2016  |  0 <= x <= 100, com valor percentual |
|  ROI 60 Dias 2017 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2017  |  0 <= x <= 100, com valor percentual |
|  ROI 60 Dias 2018 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2018  |  0 <= x <= 100, com valor percentual  |
|  ROI 60 Dias 2019 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2019  |  0 <= x <= 100, com valor percentual |
|  ROI 60 Dias 2020 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2020  |  0 <= x <= 100, com valor percentual  |
|  ROI 60 Dias Médio |  Roi médio  |  0 <= x <= 100, com valor percentual  |


bitcoin_roi_90_dias_mensal_2014-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Meses |  Meses do Ano  | Mes |
|  ROI 90 Dias 2014 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2014  |  0 <= x <= 100, com valor percentual |
|  ROI 90 Dias 2015 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2015  |  0 <= x <= 100, com valor percentual |
|  ROI 90 Dias 2016 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2016  |  0 <= x <= 100, com valor percentual |
|  ROI 90 Dias 2017 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2017  |  0 <= x <= 100, com valor percentual  |
|  ROI 90 Dias 2018 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2018  |  0 <= x <= 100, com valor percentual  |
|  ROI 90 Dias 2019 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2019  |  0 <= x <= 100, com valor percentual  |
|  ROI 90 Dias 2020 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2020  |  0 <= x <= 100, com valor percentual  |
|  ROI 90 Dias Médio |  Roi médio  |  0 <= x <= 100, com valor percentual  |

bitcoin_roi_anual_2014-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Ano |  Ano  | YYYY  |
|  ROI |  ROI médio de cada ano  | 0 <= x <= 100, com valor percentual |
|  Preço Inicial |  preço inicial no inicio de cada ano  | 0 <= x <= 100, com valor percentual |

cardano_price_marketcap_volume_20171018_20210528.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Data|  Data  | dd-mm-yyyy h-m-s-ms |
|  ADAUSD |  Valor da Cardano em dólares | >=0 |
|  marketcap |  Valor total de mercado de uma moeda | >=0 |
|  volume |  Total de moedas trocadas num determinado período de tempo |  >=0  |

cardano_roi_30_dias_mensal_2018-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Meses |  Meses do Ano  | Mes |
|  ROI 30 Dias 2018 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2018  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2019 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2019  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2020 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2020  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias Médio |  Roi médio  |  0 <= x <= 100, com valor percentual  |

cardano_roi_60_dias_mensal_2018-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Meses |  Meses do Ano  | Mes |
|  ROI 60 Dias 2018 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2018  |  0 <= x <= 100, com valor percentual  |
|  ROI 60 Dias 2019 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2019  |  0 <= x <= 100, com valor percentual |
|  ROI 60 Dias 2020 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2020  |  0 <= x <= 100, com valor percentual  |
|  ROI 60 Dias Médio |  Roi médio  |  0 <= x <= 100, com valor percentual  |

cardano_roi_90_dias_mensal_2018-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Meses |  Meses do Ano  | Mes |
|  ROI 90 Dias 2018 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2018  |  0 <= x <= 100, com valor percentual  |
|  ROI 90 Dias 2019 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2019  |  0 <= x <= 100, com valor percentual  |
|  ROI 90 Dias 2020 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2020  |  0 <= x <= 100, com valor percentual  |
|  ROI 90 Dias Médio |  Roi médio  |  0 <= x <= 100, com valor percentual  |

cardano_roi_anual_2018-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Ano |  Ano  | YYYY  |
|  ROI |  ROI médio de cada ano  | 0 <= x <= 100, com valor percentual |
|  Preço Inicial |  preço inicial no inicio de cada ano  | 0 <= x <= 100, com valor percentual |

ethereum_price_marketcap_volume_20150807_20210528.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  data |  Data | DD-MM-YYYY h-m-s-ms |
|  ETHUSD |  Valor da Ethereum em dólares | >=0 |
|  marketcap |  Valor total de mercado de uma moeda | >=0 |
|  volume |  Total de moedas trocadas num determinado período de tempo |  >=0  |

ethereum_roi_30_dias_mensal_2016-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Ano |  Ano  |  YYYY  |
|  Meses |  Meses do Ano  | Mes |
|  ROI 30 Dias 2014 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2014  |0 <= x <= 100, com valor percentual   |
|  ROI 30 Dias 2015 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2015  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2016 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2016  | 0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2017 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2017  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2018 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2018  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2019 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2019  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias 2020 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 30 dias depois no ano 2020  |  0 <= x <= 100, com valor percentual  |
|  ROI 30 Dias Médio |  Roi médio  |  0 <= x <= 100, com valor percentual  |

ethereum_roi_60_dias_mensal_2016-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Meses |  Meses do Ano  | Mes |
|  ROI 60 Dias 2014 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2014  |  0 <= x <= 100, com valor percentual |
|  ROI 60 Dias 2015 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2015  |  0 <= x <= 100, com valor percentual  |
|  ROI 60 Dias 2016 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2016  |  0 <= x <= 100, com valor percentual |
|  ROI 60 Dias 2017 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2017  |  0 <= x <= 100, com valor percentual |
|  ROI 60 Dias 2018 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2018  |  0 <= x <= 100, com valor percentual  |
|  ROI 60 Dias 2019 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2019  |  0 <= x <= 100, com valor percentual |
|  ROI 60 Dias 2020 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 60 dias depois no ano 2020  |  0 <= x <= 100, com valor percentual  |
|  ROI 60 Dias Médio |  Roi médio  |  0 <= x <= 100, com valor percentual  |


ethereum_roi_90_dias_mensal_2016-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Meses |  Meses do Ano  | Mes |
|  ROI 90 Dias 2014 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2014  |  0 <= x <= 100, com valor percentual |
|  ROI 90 Dias 2015 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2015  |  0 <= x <= 100, com valor percentual |
|  ROI 90 Dias 2016 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2016  |  0 <= x <= 100, com valor percentual |
|  ROI 90 Dias 2017 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2017  |  0 <= x <= 100, com valor percentual  |
|  ROI 90 Dias 2018 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2018  |  0 <= x <= 100, com valor percentual  |
|  ROI 90 Dias 2019 | ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2019  |  0 <= x <= 100, com valor percentual  |
|  ROI 90 Dias 2020 |  ROI tendo em conta a data de investimento inicial o dia 1 de cada mês e a venda do mesmo 90 dias depois no ano 2020  |  0 <= x <= 100, com valor percentual  |
|  ROI 90 Dias Médio |  Roi médio  |  0 <= x <= 100, com valor percentual  |

ethereum_roi_anual_2016-2020.csv

| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  Ano |  Ano  | YYYY  |
|  ROI |  ROI médio de cada ano  | 0 <= x <= 100, com valor percentual |
|  Preço Inicial |  preço inicial no inicio de cada ano  | 0 <= x <= 100, com valor percentual |



## 💡 Problemas, inconsistências e melhorias 💡 

Alguns problemas que necessitaram de atenção foi principalmente alguns dados que continham informação inútil (para este trabalho), a necessidade de conversão das datas em epoch e a ausência de alguns dados em certos dias de 2017 nos dados fornecidos pela API da Coingecko.





