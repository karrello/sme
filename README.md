# sme
Karrello for Sonor Music Editions

Configuration file: [`_data/karrello.yml`](https://github.com/karrello/sme/blob/main/_data/karrello.yml)

```yml
merchant: sb-vpvzq3424491@business.example.com

# Currency use three-character ISO-4217 codes
currency:
  code: EUR
  symbol: €

# Collections enabled to sell
collections:
  - catalog

# Items number for wholesale prices and shipping
wholesale:
  price: 3
  shipping: 6

# Max item quantity
max: 10

# Prices for every support
price:
  lp:
    few: 15
    many: 9
  dlp:
    few: 20
    many: 16

# Shipping prices
shipping:
  italy:
    few: 10
    many: 15
  europe:
    few: 15
    many: 20
  world:
    few: 20
    many: 40
```

#### Documentation

- [Archived **JavaScriptButtons** repository](https://web.archive.org/web/20161004203013/https://github.com/paypal/JavaScriptButtons)
- [Archived **HTML variables** Dev Docs](https://web.archive.org/web/20161227211543/https://developer.paypal.com/docs/classic/paypal-payments-standard/integration-guide/Appx_websitestandard_htmlvariables/)