# Desafio de Web Scraping

Este desafio tem por objetivo avaliar as habilidades do candidato para construir rotinas de _Web Scraping_.

## Introdução

Deve-se construir uma rotina para coletar dados de criptomoedas através do site [CoinMarketCap](https://coinmarketcap.com/). O resultado do processo deve ser um arquivo JSON cujo conteúdo deve seguir o modelo abaixo:

```json
{
  "name": "Bitcoin",
  "code": "BTC",
  "price": 20948.79,
  "1h%": -0.19,
  "24h%": -4.22,
  "7d%": -10.23,
  "marketCap": 400437535682,
  "volume24h": 40242256917,
  "circulatingSupply": 19104093,
  "markets": [
    {
      "source": "Binance",
      "pairs": "BTC/USDT",
      "price": 20916.72,
      "+2%depth": 20586463.72,
      "-2%depth": 27413312.35,
      "volume": 4182018204,
      "volume%": 10.41,
      "confidence": "High",
      "liquidity": 984,
      "updated": "Recently"
    }
  ]
}
```
