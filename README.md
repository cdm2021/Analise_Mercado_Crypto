# 💰 Análise do mercado de crypto 💰

## 📋 Recolha de dados 📋
Os dados foram recolhidos através do site coingecko (https://www.coingecko.com/pt) onde foi feito um “request” de dados sobre o preço, volume e "market cap" de diversas cryptomoedas. Foram feitos mais "requests" de preço, volume e "market cap" históricos das moedas Bitcoin e Ethereum. Para o caso do Bitcoin a base de dados pedida foi entre 2014 até 2021. Já no caso do Ethereum, por ser uma moeda mais recente, a base de dados pedida apenas abrange dados entre 2016 até 2021. Todos foram fornecidos através do formato .json.

A Coingecko é uma plataforma que fornece uma análise fundamental do mercado de criptomoedas. Além de acompanhar preços, volume e capitalização de mercado, a CoinGecko acompanha o crescimento da comunidade, desenvolvimento do código-fonte aberto, principais eventos e métricas em cadeia.

Limpámos alguns dados que não eram relevantes para este projeto de forma a conseguirmos uma base de dados mais limpa e fácil de trabalhar no nosso objetivo.

## 🤔 Contexto 🤔 
Com o crescente interesse em criptoativos, durante o ano de 2020, decidimos realizar o nosso trabalho de forma a explorar alguns dados estatisticos relacionados com o tema.
A maioria dos sites que faz o reportório deste tipo de dados disponibiliza-os de uma forma geral e oferece pouca organização destas informações, desta forma também ficam mais facilmente inspeccionáveis/manipuláveis. Sem este tipo de trabalho tornam-se dificultadas as tarefas de análise, modelação e visualização por parte da comunidade de criptomoedas.

Como as API estão disponiveis na nuvem destes websites, então não é necessário descarregar-las e fica fácil para qualquer utilizador que quiser aceder a estes dados relativamente aos seus investimentos nesta área a partir do github.

A estrutura base deste ficheiro, desenhada para fácil manipulação em Excel/Python/R, não mudará, podendo a comunidade analítica considerá-lo um alvo imutável (em termos de localização e estrutura) para, por exemplo, alimentar plataformas de visualização/modelação. De notar que, mediante no final do ano 2021 com os relatórios da situação que irão decorrer, poderão ser adicionadas novas colunas desde que fornecidas pelo mesmo website e tratadas da mesma forma, mantendo-se claro a retrocompatibilidade. Fontes adicionais de dados poderão também então ser adicionadas.

Porque todas as boas decisões começam com bons dados.

## 🧱 Estrutura 🧱
Análise de mercado de cryptomoedas em relação a MarketShare:(https://github.com/cdm2021/Crypto_2020_2semestre/blob/main/An%C3%A1lise%20de%20mercado%20de%20cryptomoedas%20no%20geral.ipynb).

Preço, Volume e ROI Anual, de 30, 60 e 90 dias do par BTC-USD:(https://github.com/cdm2021/Crypto_2020_2semestre/blob/main/Pre%C3%A7o,%20Volume%20e%20ROI%20Anual,%20de%2030,%2060%20e%2090%20dias%20do%20par%20BTC-USD.ipynb).

Preço, Volume e ROI Anual, de 30, 60 e 90 dias do par ETH-USD:(https://github.com/cdm2021/Crypto_2020_2semestre/blob/main/Pre%C3%A7o,%20Volume%20e%20ROI%20Anual,%20de%2030,%2060%20e%2090%20dias%20do%20par%20ETH-USD.ipynb).

## 🚀 Funções das aplicações 🚀
Aviso Legal: Este trabalho nao tem como intuito de dar aconcelhamento financeiro, tem apenas o intuito de verificar dados de ação de preço ao longo dos anos.

Análise de mercado de cryptomoedas em relação a MarketShare - Representação gráfica e atualizada de partilha de mercado entre as 100 maiores Criptomoedas em 2020. O uso de "others" serve para simplificar o gráfico e obter uma melhor visualização sobre as moedas que com maior valor total de mercado.

Preço, Volume e ROI Anual, de 30, 60 e 90 dias do par BTC-USD - Preço e Volume de negócio da Bitcoin histórico desde 01/01/2014 até 01/03/2021. Foi necessário fazer request dos dados até ao mês de março para poder fazer o cálculo de ROI de 60 e 90 dias. O ROI foi calculado a partir do dia 1 de cada mês e acabando 30/60/90 dias depois. O cálculo e representação visual do ROI feito no nosso trabalho é uma ferramenta que pode ajudar em futuros investimentos, tendo em conta a ação de preço nos anos anteriores. 

Preço, Volume e ROI Anual, de 30, 60 e 90 dias do par ETH-USD - Preço e Volume de negócio da Ethereum histórico desde 01/01/2016 até 01/03/2021. Tal como no caso do Bitcoin, foi necessário fazer request dos dados até ao mês de março para poder fazer o cálculo de ROI de 60 e 90 dias. O ROI foi calculado a partir do dia 1 de cada mês e acabando 30/60/90 dias depois. O cálculo e representação visual do ROI feito no nosso trabalho é uma ferramenta que pode ajudar em futuros investimentos, tendo em conta a ação de preço nos anos anteriores. 

## 📔 Dicionário dos dados 📔
| Nome do ficheiro  |  Função e contéudo  |  Possiveis Valores  |
| ------------------- | ------------------- | ----------------- |
|  data |  Data | DD-MM-YYYY  |
|  BTCUSD |  Valor da Bitcoin em dólares |  Inteiro >=0 |

## 💡 Problemas, inconsistências e melhorias 💡 
